# 概要

DXライブラリ HTML5版を使ったゲーム開発をするために、DXライブラリ HTML5版に必要なライブラリをインストールするところから、サンプルコードをビルドするところまでの手順を説明します。

なお、DXライブラリ HTML5版およびemscripten 用のプロジェクトテンプレートはまだ製作段階です。手元の環境でのみ動作確認が取れていないため、動作確認およびバグや使いづらいところの指摘をコメント欄に投稿していただきますようお願いいたします。

## 動作確認済みの環境

- Windows 10 Education (Version 10.0.17763.1098) 
- Visual Studio 2017 Community (Version 15.9.21)

## 手順/目次

- [emscripten をインストールする](#emscripten-をインストールする)
- [emscripten 用のプロジェクトテンプレートをインストールする](##emscripten-用のプロジェクトテンプレートをインストールする)
- [DXライブラリ HTML5版をダウンロードする](#dxライブラリ-html5版をダウンロードする)
- [DXライブラリ HTML5版を使うためのプロジェクト設定](#dxライブラリ-html5版を使うためのプロジェクト設定)
- [ソースコードを書く](#ソースコードを書く)
- [ビルドとデバッグ](#ビルドとデバッグ)
- [トラブルシューティング](#トラブルシューティング)

# emscripten をインストールする

emscripten をインストールするのに、emscripten SDK (emsdk) を使います。
emscripten SDK (emsdk) 自体は python スクリプトで書かれています。そのため、emscripten SDK (emsdk) を使うために python をインストールする必要があります。

## python のインストール

<https://www.python.jp/install/windows/install_py3.html> に、Python のインストール方法が書かれています。
遷移先のサイトの指示に従って、Python をインストールしてください。インストールする際には、`Add python into PATH`(Python を環境変数 PATH に登録する) にチェックマークをつけることを忘れないでください[^customize-python-install]。

![python-install](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/19fd629e-4652-999e-c53e-9213a288049a.png)

[^customize-python-install]: python のインストールをカスタマイズする際、次の設定を有効にしてください。

  - pip をインストールする
  - 環境変数に python のパスに追加する

  ![InstallPIP.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/e1ee35e4-affa-bf8f-0e55-2feb21ce7196.png)

## emscripten SDK (emsdk) のインストール

[GitHub - emscripten-core/emsdk](https://github.com/emscripten-core/emsdk/)に移動し、緑色の `Code` ボタン、`Download ZIP` ボタンを順に押してください。[^emsdk-git]
すると、リポジトリの内容が .zip ファイルでダウンロードされるので、適当なフォルダに展開してください。

[^emsdk-git]: git をインストールしている環境であれば、`git clone https://github.com/emscripten-core/emsdk.git`でダウンロードすることができます。

![InstallEMSDK1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/4b923473-ecf0-0266-950e-e5a8044ec60f.png)

## emscripten のインストール

エクスプローラを開き、emscripten SDK (emsdk) をダウンロードしたディレクトリに移動し、アドレスバーに `cmd` と入力して、コマンドプロンプトを開きます。

![launch-cmd](https://siv3d.kamenokosoft.com/assets/img/building/get-emscripten/launch-cmd.png)

コマンドプロンプトを開いたら、次のコマンドを実行します。

```bat:cmd.exe
emsdk install 2.0.4
emsdk activate 2.0.4 --permanent
```

`emsdk install 2.0.4` で、emscripten 本体と emscripten で使われる clang、node.js、javaがインストールされます。
`emsdk activate 2.0.4 --permanent` で、インストールしたツールセットのセットアップが行われます。

# emscripten 用のプロジェクトテンプレートをインストールする

Visual Studio が emscripten に付随する emcc を使ってコンパイルを行うようにするために、**Emscripten Extension Pack for Visual Studio** Visual Studio 機能拡張をインストールします。

[Visual Studio Market Place](https://marketplace.visualstudio.com/items?itemName=KamenokoSoft.emscripten-extensions) から .vsix パッケージをダウンロードします[^install-via-extension-manager]。

[^install-via-extension-manager]: Visual Studio において、[ツール] > [拡張機能と更新プログラム] から拡張機能マネージャを開いて、そこで `Emscripten Extension Pack for Visual Studio` と検索しても、この拡張機能をインストールすることができます。

  ![setup-vs-ext-1.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/setup-vs-ext-1.png)
  ![VisualStudioExtensionManager0.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/VisualStudioExtensionManager0.png)

![VisualStudioExtensionInstaller0_ja.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/VisualStudioExtensionInstaller0_ja.png)

ダウンロードした .vsix パッケージを実行します。すると、インストールする拡張機能を尋ねるウィンドウが出てくるので、すべてのチェックボックスにチェックがついた状態で **Modify** と書かれたボタンをクリックします。

![VisualStudioExtensionInstaller1_ja.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/VisualStudioExtensionInstaller1_ja.png)

**Emscripten Debugger for Visual Studio** と **Emscripten Build Support** のインストールが成功していることを確認して、**Close** と書かれたボタンをクリックします。

![VisualStudioExtensionInstaller2_ja.png](https://siv3d.kamenokosoft.com/assets/img/building/setup-visualstudio/VisualStudioExtensionInstaller2_ja.png)

# DXライブラリ HTML5版をダウンロードする

DXライブラリ HTML5版本体は [nokotan/DxLibForHTML5 releases](https://github.com/nokotan/DxLibForHTML5/releases/) からダウンロードできます。
適当なフォルダに展開してください。

# DXライブラリ HTML5版を使うためのプロジェクト設定

ここからは、**DXライブラリ HTML5版をダウンロードフォルダ `%USERPROFILE%\Downloads` にインストールした場合**の説明を行います。

## emscripten ツールチェインの登録

[プロジェクト] > [プロパティ] から、プロジェクト設定を開きます。

プロジェクト設定の、[全般] > [emscripten ツールチェイン] > [emscripten インストールディレクトリ] に、インストールした emscripten のフォルダ (emcc.bat ファイルが存在するフォルダ) へのパスを入力します。

![Siv3DWebProjectMake3.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/74993f9c-8ff4-e500-3521-8f0e7748a403.png)

## インクルードディレクトリ/コンパイラ設定

[Emscripten C/C++] > [全般] > [追加のインクルードディレクトリ] に次のフォルダを指定します。

```txt:追加のインクルードディレクトリ
$(USERPROFILE)\Downloads\DxLibForHTML5\dest\include
```

![DxLibHTML5inc.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/a47a5659-d1de-43b6-3031-d7922fc00b4c.png)

## ライブラリディレクトリ/リンカ設定

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

# ソースコードを書く

DXライブラリ HTML5版では、DXライブラリ Android版で使用できる関数 (Android版専用の関数を除く) が使用できます。

ただし、イベント処理のために定期的にブラウザに制御を戻す必要があります。そのため、**メインループ部分を関数に切り出し**、その関数を**フレーム開始時に呼ばれるコールバック関数として登録**する必要があります。

```c++:Main.cpp
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

# ビルドとデバッグ

ビルドは Windows 版と同じように [ビルド] > [ソリューションのビルド] でできます。
また、[|> WebAssembly Debugger] をクリックして、ビルドおよびデバッグ実行を行えます。
デバッグ実行では、次の操作が可能です。

- ブレークポイントの設置
- 変数の値のダンプ

![run-on-vs-1.png](https://siv3d.kamenokosoft.com/assets/img/building/running-code-with-visualstudio/run-on-vs-1.png)
