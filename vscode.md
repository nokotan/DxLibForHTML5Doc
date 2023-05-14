# Visual Studio をセットアップする

## 概要

DXライブラリ HTML5版を使ったゲーム開発をするために、DXライブラリ HTML5版に必要なライブラリをインストールするところから、サンプルコードをビルドするところまでの手順を説明します。

## emscripten をインストールする

emscripten をインストールするのに、emscripten SDK (emsdk) を使います。
emscripten SDK (emsdk) 自体は python スクリプトで書かれています。そのため、emscripten SDK (emsdk) を使うために python をインストールする必要があります。

### python のインストール

<https://www.python.jp/install/windows/install_py3.html> に、Python のインストール方法が書かれています。
遷移先のサイトの指示に従って、Python をインストールしてください。インストールする際には、`Add python into PATH`(Python を環境変数 PATH に登録する) にチェックマークをつけることを忘れないでください[^customize-python-install]。

![python-install](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/19fd629e-4652-999e-c53e-9213a288049a.png)

[^customize-python-install]: python のインストールをカスタマイズする際、次の設定を有効にしてください。

  - pip をインストールする
  - 環境変数に python のパスに追加する

  ![InstallPIP.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/e1ee35e4-affa-bf8f-0e55-2feb21ce7196.png)

### emscripten SDK (emsdk) のインストール

[GitHub - emscripten-core/emsdk](https://github.com/emscripten-core/emsdk/)に移動し、緑色の `Code` ボタン、`Download ZIP` ボタンを順に押してください。
すると、リポジトリの内容が .zip ファイルでダウンロードされるので、適当なフォルダに展開してください。

![InstallEMSDK1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/4b923473-ecf0-0266-950e-e5a8044ec60f.png)

### emscripten のインストール

エクスプローラを開き、emscripten SDK (emsdk) をダウンロードしたディレクトリに移動し、アドレスバーに `cmd` と入力して、コマンドプロンプトを開きます。

![launch-cmd](https://siv3d.kamenokosoft.com/assets/img/building/get-emscripten/launch-cmd.png)

コマンドプロンプトを開いたら、次のコマンドを実行します。

```bat:cmd.exe
emsdk install 3.1.20
emsdk activate 3.1.20 --permanent
```

`emsdk install 3.1.20` で、emscripten 本体と emscripten で使われる clang、node.js、javaがインストールされます。
`emsdk activate 3.1.20 --permanent` で、インストールしたツールセットのセットアップが行われます。

## 拡張機能のインストール

Visual Studio Code の左側の拡張機能タブから、次の名前で検索し、インストールしてください。

- C/C++ VSCode Extension
- WebAssembly on Chrome Debugger (実行に Chrome を使う場合)
- Debugger for Firefox (実行に FireFox を使う場合)

![install-extension.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/bf97ad48-9626-4898-d671-48b740ddaecc.png)

## DxLib for HTML5 Visual Studio Code サンプルプログラム実行用パッケージを Visual Studio Code で開く

### DxLib for HTML5 Visual Studio Code サンプルプログラム実行用パッケージをダウンロードする

[サンプルプログラム実行用パッケージのリポジトリ](https://github.com/nokotan/DxLibForHTML5-VSCode) に移動し、緑色の "Code" ボタン、"Download ZIP" ボタンを順に押してください。

すると、リポジトリの内容が .zip ファイルでダウンロードされるので、適当なフォルダに展開してください。

![スクリーンショット 2020-08-13 16.34.04.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/9acb0a88-8403-b3b3-ce59-4a5bc3992bce.png)

### DxLib for HTML5 Visual Studio Codeサンプルプログラム実行用パッケージを Visual Studio Codeで開く

Visual Studio Code を起動して、[ファイル] > [フォルダを開く...] でフォルダを開くためのダイアログを表示します。

![open-vscode.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/158514/385e8dfe-3f3a-431f-a8ed-63e2d491723c.png)

ここで、先ほど展開した DxLib for HTML5 Visual Studio Codeサンプルプログラム実行用パッケージが含まれるフォルダを選んでください。

## ソースコードを書く

DXライブラリ HTML5版では、DXライブラリ Android版で使用できる関数 (Android版専用の関数を除く) が使用できます。

ただし、イベント処理のために定期的にブラウザに制御を戻す必要があります。そのため、**メインループ部分を関数に切り出し**、その関数を**フレーム開始時に呼ばれるコールバック関数として登録**する必要があります。

```c++:Main.cpp
#include "DxLib.h"

#ifdef EMSCRIPTEN
#  include <emscripten.h>
#endif

static bool shouldExit = false;

void mainLoop() {
	if (ProcessMessage() == -1) {
		shouldExit = true;
	}

	ClearDrawScreen();

	{
		int MouseX, MouseY;
		int CircleColor = (GetMouseInput() & MOUSE_INPUT_LEFT) ? GetColor(255, 255, 0) : GetColor(255, 0, 0);

		GetMousePoint(&MouseX, &MouseY);
		DrawCircle(MouseX, MouseY, 64, CircleColor);
	}

	{
		int StringColor = CheckHitKey(KEY_INPUT_SPACE) ? GetColor(0, 255, 0) : GetColor(255, 255, 255);
		DrawString(3, 3, "Hello DxLib on HTML5!", StringColor);
	}

	ScreenFlip();
}

#ifdef _WIN32
int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int) {
#else
int main () {
#endif
	SetGraphMode(640, 480, 32);

    if (DxLib_Init() == -1) {
		return -1;
    }

    ChangeFont("07LogoTypeGothic7.ttf");
	SetDrawScreen(DX_SCREEN_BACK);

#ifdef EMSCRIPTEN
	emscripten_set_main_loop(mainLoop, 0, 1);	
#else
    while (!shouldExit) {
		mainLoop();
    }
    
    DxLib_End();
 #endif

    return 0;
}
```

## ビルドとデバッグ実行

### ビルド

ビルドは、次の方法があります。

- [Ctrl]+[Shift]+[B] を押す
- Ctrl(Cmd)+Shift+P でタスクの実行を選んで, `Build: Debug (or Release)` を選ぶ

![vscode-run-task.png](https://siv3d.kamenokosoft.com/assets/img/building/running-code-with-vscode/vscode-run-task.png)

![vscode-run-task-2.png](https://siv3d.kamenokosoft.com/assets/img/building/running-code-with-vscode/vscode-run-task-2.png)

### デバッグなしでプロジェクトを実行する

Ctrl(Cmd)+Shift+P でタスクの実行を選んで, **Run Local Server and Open Browser** を選びます。

### プロジェクトを実行し、VScode でデバッグする

VScode でのデバッグは、Chrome と FireFox でのみ有効です。

#### Chrome

実行とデバッグ タブで Launch Chrome against localhost を選択して、▶️ を押します。

![start-debugging.png](https://siv3d.kamenokosoft.com/assets/img/building/running-code-with-vscode/start-debugging.png)

### FireFox

実行とデバッグ タブで Launch Chrome against localhost を選択して、▶️ を押します。
FireFox 上でのデバッグは、ソースマップのみ有効になります。

## 公開に関する注意

DxLibForHTML5 では、SharedArrayBuffer を使用しており、サーバ側にレスポンスヘッダの設定が必要です。

- [SharedArrayBuffer を使用するための必要要件](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer)
- [COOP ヘッダ](https://developer.mozilla.org/ja-JP/docs/Web/HTTP/Headers/Cross-Origin-Opener-Policy)
- [COEP ヘッダ](https://developer.mozilla.org/ja-JP/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy)
