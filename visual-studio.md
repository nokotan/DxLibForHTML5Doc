# Visual Studio をセットアップする

## 概要

DXライブラリ HTML5版を使ったゲーム開発をするために、DXライブラリ HTML5版に必要なライブラリをインストールするところから、サンプルコードをビルドするところまでの手順を説明します。

なお、DXライブラリ HTML5版および emscripten 用のプロジェクトテンプレートはまだ製作段階です。手元の環境でのみ動作確認が取れていないため、動作確認およびバグや使いづらいところの指摘をコメント欄に投稿していただきますようお願いいたします。

## emscripten をインストールする

Windows 向け Emscripten 3.1.20 インストーラが [GitHub Releases](https://github.com/nokotan/EmscriptenInstaller/releases/latest) からダウンロードできます。

<details markdown="block"><summary>Emscripten 3.1.20 インストーラが行う処理</summary>

インストーラは次のツールをお使いの開発環境にダウンロードします。

- Emscripten 3.1.20
- Clang Compiler Front End
- Node
- Python

</details>

Assets リスト中の `EmscriptenOffline.exe` をクリックしてダウンロードします。
お使いのネットワークによっては、ダウンロードに10分以上かかることがあります。

![EmscriptenInstallerGitHub](https://siv3d.kamenokosoft.com/assets/img/building/install-emscripten/EmscriptenInstallerGitHub.png)

`EmscriptenOffline.exe` がダウンロード出来たら、ダブルクリックして実行します。

## emscripten 用のプロジェクトテンプレートをインストールする

Visual Studio が emscripten に付随する emcc を使ってコンパイルを行うことができるようにするために、**Emscripten Extension Pack for Visual Studio** Visual Studio 機能拡張をインストールします。

[Visual Studio Market Place](https://marketplace.visualstudio.com/items?itemName=KamenokoSoft.emscripten-build-support) から .vsix パッケージをダウンロードします。

![InstallBuildSupport1.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/InstallBuildSupport1.png)

.vsix パッケージがダウンロードできたら、ダブルクリックして実行します。

## DXライブラリ HTML5版をダウンロードする

DXライブラリ HTML5版本体は [nokotan/DxLibForHTML5 releases](https://github.com/nokotan/DxLibForHTML5/releases/) からダウンロードできます。
適当なフォルダに展開してください。

## DXライブラリ HTML5版を使うためのプロジェクト設定

ここからは、**DXライブラリ HTML5版をダウンロードフォルダ `%USERPROFILE%\Downloads` にインストールした場合**の説明を行います。

### emscripten ツールチェインの登録

[プロジェクト] > [プロパティ] から、プロジェクト設定を開きます。

プロジェクト設定の、[全般] > [emscripten ツールチェイン] > [emscripten インストールディレクトリ] に、インストールした emscripten のフォルダ (emcc.bat ファイルが存在するフォルダ) へのパスを入力します。

![Siv3DWebProjectMake3.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/74993f9c-8ff4-e500-3521-8f0e7748a403.png)

### インクルードディレクトリ/コンパイラ設定

[Emscripten C/C++] > [全般] > [追加のインクルードディレクトリ] に次のフォルダを指定します。

```txt:追加のインクルードディレクトリ
$(USERPROFILE)\Downloads\DxLibForHTML5\dest\include
```

![DxLibHTML5inc.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/a47a5659-d1de-43b6-3031-d7922fc00b4c.png)

### ライブラリディレクトリ/リンカ設定

[Emscripten リンカ] > [全般] > [追加のライブラリディレクトリ] に次の設定を追記します。

```txt:追加のライブラリディレクトリ
$(USERPROFILE)\Downloads\DxLibForHTML5\dest\bin
```

[Emscripten リンカ] > [入力] > [追加の依存ファイル] に次の設定を追記します。

```txt:追加の依存ファイル
DxLib;DxDrawFunc;DxUseCLib
```

[Emscripten リンカ] > [システム] > [メモリ伸張の有効化] を `はい` に切り替えます。

[Emscripten リンカ] > [詳細設定] > [emrun の有効化] を `はい` に切り替えます。

[Emscripten リンカ] > [コマンド ライン] > [追加のオプション] に次の設定を追記します。

```txt:追加のオプション
-s USE_OGG=1 -s USE_VORBIS=1 -s USE_LIBPNG=1 -s USE_LIBJPEG=1 -s USE_ZLIB=1 -s USE_BULLET=1 -s USE_FREETYPE=1 -s FULL_ES2=1
```

以下、オプションの説明です。

|オプション|説明|
|:--:|:----:|
|`-s USE_OGG=1 -s USE_VORBIS=1 -s USE_LIBPNG=1 -s USE_LIBJPEG=1 -s USE_ZLIB=1 -s USE_BULLET=1 -s USE_FREETYPE=1`| emscripten 側に用意されているライブラリをリンクします (Ogg, Vorbis, libpng, zlib, bullet, freetype)|
|`-s FULL_ES2=1`|OpenGLES2 のエミュレーションを有効にします|

## ソースコードを書く

DXライブラリ HTML5版では、DXライブラリ Android版で使用できる関数 (Android版専用の関数を除く) が使用できます。

ただし、イベント処理のために定期的にブラウザに制御を戻す必要があります。そのため、**メインループ部分を関数に切り出し**、その関数を**フレーム開始時に呼ばれるコールバック関数として登録**する必要があります。

```c++
# include "DxLib.h"
# include <emscripten.h>

void mainLoop() {
  if (ProcessMessage() == -1) {
    emscripten_cancel_main_loop();
    DxLib_End();
    return;
  }

  ClearDrawScreen();
  ScreenFlip();
}

int main () {
  if (DxLib_Init() == -1) {
    return -1;
  }

  SetDrawScreen(DX_SCREEN_BACK);
  emscripten_set_main_loop(mainLoop, 0, 1);
}
```

## ビルドとデバッグ

ビルドは Windows 版と同じように [ビルド] > [ソリューションのビルド] でできます。
また、[|> WebAssembly Debugger] をクリックして、ビルドおよびデバッグ実行を行えます。
デバッグ実行では、次の操作が可能です。

- ブレークポイントの設置
- 変数の値のダンプ

![run-on-vs-1.png](https://siv3d.kamenokosoft.com/assets/img/building/running-code-with-visualstudio/RunOnVS1.png)
