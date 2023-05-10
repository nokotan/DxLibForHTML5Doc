# トラブルシューティング

## インストールエラー編

### "emcc" は内部コマンドまたは外部コマンド、 操作可能なプログラムまたはバッチ ファイルとして認識されていません。と表示される

#### エラーメッセージの例

```bat:エラー例
'emcc' は内部コマンドまたは外部コマンド、 操作可能なプログラムまたはバッチ ファイルとして認識されていません。
```

```bat:エラー例
用語 'emcc' は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。
```

#### 考えられる原因

- 手順 **python のインストール** で python が正常にインストールされなかった

#### 対処方法

- [環境変数 **PATH** において、Windows にデフォルトで入っている python の優先順位を下げる](https://puarts.com/?pid=1551)

## ビルドエラー編

### No such file or directory と表示される

#### エラーメッセージの例

```txt:エラー例
shared : error : C:¥Users¥(ユーザ名)¥.emscripten_cache¥wasm-pic¥ports-builds¥zlib¥compress.c: No such file or directory
```

#### 考えられる原因

- 依存ライブラリのソースファイル群のzipファイルの展開に失敗している

#### 対処方法

- `%USERPROFILE%\.emscripten_ports` フォルダの中にある zip ファイルをその場に (画像のようにフォルダが並ぶように) 展開する
- `%USERPROFILE%\.emscripten_ports` フォルダ、`%USERPROFILE%\.emscripten_cache` フォルダを、セキュリティソフトウェアのスキャン除外フォルダに追加する

![フォルダ配置](https://camo.qiitausercontent.com/c92692163f156e6a5d5647c1866a350c81fac5d7/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e61702d6e6f727468656173742d312e616d617a6f6e6177732e636f6d2f302f3135383531342f63613539653636362d663234622d333565312d623166312d6635343165613136373933352e706e67)

## ランタイムエラー編

### 特にエラーが発生しないが画面が表示されない

#### 考えられる原因

- 現在調査中

#### 対処方法

- `-s FULL_ES2=1` の代わりに `-s FULL_ES3=1` を Emscripten リンカの追加のオプションに追加する

# 参考資料

- CLion で Emscripten をやっていきたい ( <https://qiita.com/tan-y/items/d5539ddd8ce10972919a#emscripten-sdk-%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB> )
- emscripten Download and Install ( <https://emscripten.org/docs/getting_started/downloads.html> )
- Pythonのインストール方法\[Windows\] ( <https://qiita.com/R-Imai/items/18fee5203e695838e899> )
- emscripten Running HTML files with emrun ( <https://emscripten.org/docs/compiling/Running-html-files-with-emrun.html> )
