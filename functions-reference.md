# 関数リファレンス

[DXライブラリ 公式関数リファレンス](https://dxlib.xsrv.jp/dxfunc.html) のうち、Android で利用可能なものを機械的にリストアップしたものです。(HTML5 版は Android 版がベースのため)
一部利用できない関数が対応表記になっていますがご了承ください。

## 使用必須関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [DxLib_Init](https://dxlib.xsrv.jp/dxfunc.html#R1N1) | ライブラリの初期化 |
| ○ | [DxLib_End](https://dxlib.xsrv.jp/dxfunc.html#R1N2) | ライブラリ使用の終了関数 |
| ○ | [ProcessMessage](https://dxlib.xsrv.jp/dxfunc.html#R1N3) | ウインドウズのメッセージを処理する |

## ３Ｄ関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [一覧はこちら](https://dxlib.xsrv.jp/function/dxfunc_3d.html) | 　数が多いので分けました |

## Live2D関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [一覧はこちら](https://dxlib.xsrv.jp/function/dxfunc_live2D.html) | 　 |

## 図形描画関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [DrawLine](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N1) | 　線を描画 |
| ○ | [DrawLineAA](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N1_A) | 　線を描画(アンチエイリアス効果付き) |
| ○ | [DrawBox](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N2) | 　四角を描画 |
| ○ | [DrawBoxAA](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N2_A) | 　四角を描画(アンチエイリアス効果付き) |
| ○ | [DrawCircle](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N3) | 　円の描画 |
| ○ | [DrawCircleAA](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N3_A) | 　円の描画(アンチエイリアス効果付き) |
| ○ | [DrawOval](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N4) | 　楕円の描画 |
| ○ | [DrawOvalAA](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N4_A) | 　楕円の描画(アンチエイリアス効果付き) |
| ○ | [DrawTriangle](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N7) | 　三角形の描画 |
| ○ | [DrawTriangleAA](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N7_A) | 　三角形の描画(アンチエイリアス効果付き) |
| ○ | [DrawPixel](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N5) | 　点を描画する |
| ○ | [GetPixel](https://dxlib.xsrv.jp/function/dxfunc_graph0.html#R2N6) | 　指定点の色を取得 |

## グラフィックデータ制御関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [LoadGraphScreen](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N1) | 　画像ファイルを読みこんで画面に表示する |
| ○ | [LoadGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N2) | 　画像ファイルのメモリへの読みこみ、及び動画ファイルのロード |
| ○ | [LoadDivGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N3) | 　画像ファイルのメモリへの分割読みこみ |
| ○ | [MakeGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N6) | 　空のグラフィックを作成する | 
| ○ | [MakeScreen](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N25) | 　描画対象にできるグラフィックを作成する | 
| ○ | [SetCreateDrawValidGraphMultiSample](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N32) | 　描画対象にできるグラフィックのマルチサンプリング設定を行う | 
| ○ | [SetCreateGraphColorBitDepth](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N33) | 　作成するグラフィックのビット深度を設定する | 
| | [SetDrawValidFloatTypeGraphCreateFlag](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N34) | 　描画可能な浮動小数点型のグラフィックを作成するかどうかの設定を行う | 
| ○ | [SetCreateDrawValidGraphChannelNum](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N35) | 　作成する描画可能なグラフィックのチャンネル数の設定を行う | 
| ○ | [SetUsePremulAlphaConvertLoad](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N37) | 　読み込み時に画像を乗算済みα画像に変換するかを設定する | 
| ○ | [DrawGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N7) | 　メモリに読みこんだグラフィックの描画 |
| ○ | [DrawTurnGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N8) | 　メモリに読みこんだグラフィックのＬＲ反転描画 |
| ○ | [DrawExtendGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N9) | 　メモリに読みこんだグラフィックの拡大縮小描画 |
| ○ | [DrawRotaGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N10) | 　メモリに読みこんだグラフィックの回転描画 |
| ○ | [DrawRotaGraph2](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N19) | 　メモリに読みこんだグラフィックの回転描画(回転中心指定あり) |
| ○ | [DrawRotaGraph3](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N36) | 　メモリに読みこんだグラフィックの回転描画(回転中心指定あり、縦横拡大率別指定) |
| ○ | [DrawModiGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N11) | 　メモリに読みこんだグラフィックの自由変形描画 |
| ○ | [DrawRectGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N20) | 　グラフィックの指定矩形部分のみを描画 |
| ○ | [DerivationGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N21) | 　指定のグラフィックの指定部分だけを抜き出して新たなグラフィックを作成する |
| ○ | [GetDrawScreenGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N12) | 　描画先に設定されているグラフィック領域から指定領域のグラフィックを読みこむ |
| ○ | [GetGraphSize](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N13) | 　グラフィックのサイズを得る |
| ○ | [InitGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N14) | 　読みこんだグラフィックデータをすべて削除する |
| ○ | [DeleteGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N15) | 　指定のグラフィックをメモリ上から削除する |
| ○ | [SetDrawMode](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N16) | 　描画モードをセットする |
| ○ | [SetDrawBlendMode](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N17) | 　描画の際のブレンドモードをセットする |
| ○ | [SetDrawBright](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N18) | 　描画輝度をセット |
| ○ | [SetTransColor](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R15N7) | 　グラフィックに設定する透過色をセットする |
| ○ | [LoadBlendGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N23) | 　画像ファイルからブレンド画像を読み込む |
| ○ | [DrawBlendGraph](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N24) | 　ブレンド画像と通常画像を合成して描画する |
| ○ | [GraphFilter](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N26) | 　画像にフィルター処理を施す |
| ○ | [GraphFilterBlt](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N27) | 　画像にフィルター処理を施す( 出力先画像指定版 ) |
| ○ | [GraphFilterRectBlt](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N28) | 　画像にフィルター処理を施す( 出力先画像、使用矩形指定版 ) |
| ○ | [GraphBlend](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N29) | 　二つの画像を特殊効果付きでブレンドする |
| ○ | [GraphBlendBlt](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N30) | 　二つの画像を特殊効果付きでブレンドする( 出力先画像指定版 ) |
| ○ | [GraphBlendRectBlt](https://dxlib.xsrv.jp/function/dxfunc_graph1.html#R3N31) | 　二つの画像を特殊効果付きでブレンドする( 出力先画像、使用矩形指定版 ) |

## 文字描画関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [DrawString](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N1) | 　文字列を描画する |
| ○ | [DrawFormatString](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N20) | 　書式付き文字列を描画する |
| ○ | [GetDrawStringWidth](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N2) | 　DrawString で描画される文字列の幅(ドット単位)を得る |
| ○ | [GetDrawFormatStringWidth](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N21) | 　DrawFormatString 関数書式付き文字列の描画幅(ドット単位)を得る |
| ○ | [SetFontSize](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N7) | 　描画する文字列のサイズをセットする |
| ○ | [SetFontThickness](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N8) | 　描画する文字列の文字の太さをセットする |
| ○ | [ChangeFont](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N9) | 　描画するフォントを変更する |
| ○ | [ChangeFontType](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N24) | 　文字列描画に使用するフォントのタイプを変更する |
| ○ | [CreateFontToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N10) | 　新しいフォントデータを作成 |
| ○ | [LoadFontDataToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N26) | 　ＤＸフォントデータファイルを読み込む |
| ○ | [DeleteFontToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N11) | 　フォントデータを削除する |
| ○ | [SetFontCacheUsePremulAlphaFlag](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N25) | 　作成するフォントデータを『乗算済みα』用にするかどうかを設定する |
| ○ | [DrawStringToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N12) | 　指定のフォントデータで文字列を描画する |
| ○ | [DrawFormatStringToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N22) | 　指定のフォントデータで書式付き文字列を描画する |
| ○ | [GetDrawStringWidthToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N13) | 　指定のフォントデータで描画する文字列の幅を得る |
| ○ | [GetDrawFormatStringWidthToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N23) | 　指定のフォントデータで書式付き文字列の描画幅を得る |
| ○ | [GetFontStateToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N18) | 　指定のフォントデータの情報を得る |
| ○ | [InitFontToHandle](https://dxlib.xsrv.jp/function/dxfunc_graph2.html#R17N19) | 　フォントデータを全て初期化する |

## 簡易画面出力関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [printfDx](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R18N1) | 　簡易文字列描画 |
| ○ | [clsDx](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R18N2) | 　簡易画面出力履歴をクリアする |

## その他画面操作系関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [SetGraphMode](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N1) | 　画面モードの変更 |
| | [SetFullScreenResolutionMode](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N10) | 　フルスクリーンモード時の解像度モードを設定する |
| ○ | [SetFullScreenScalingMode](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N11) | 　フルスクリーンモード時の画面拡大モードを設定する |
| ○ | [GetScreenState](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N2) | 　現在の画面の大きさとカラービット数を得る |
| ○ | [SetDrawArea](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N3) | 　描画可能領域のセット |
| ○ | [ClearDrawScreen](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N4) | 　画面に描かれたものを消去する |
| ○ | [ClearDrawScreenZBuffer](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N12) | 　深度バッファをクリアする |
| ○ | [SetBackgroundColor](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N9) | 　画面の背景色を設定する |
| ○ | [GetColor](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N5) | 　色コードを取得する |
| ○ | [SetDrawScreen](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N6) | 　描画先グラフィック領域の指定 |
| ○ | [ScreenFlip](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N7) | 　フリップ関数、画面の裏ページ(普段は表示されていない)の内容を表ページ(普段表示されている)に反映する |
| | [SetFullSceneAntiAliasingMode](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R4N8) | 　画面のフルスクリーンアンチエイリアスモードの設定をする |

## 動画関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [PlayMovie](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N1) | 　動画ファイルの再生 |
| ○ | [PlayMovieToGraph](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N2) | 　ムービーグラフィックの動画の再生を開始する |
| ○ | [PauseMovieToGraph](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N3) | 　ムービーグラフィックの動画再生を一時停止する |
| ○ | [SeekMovieToGraph](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N4) | 　ムービーグラフィックの動画の再生位置を変更する |
| ○ | [TellMovieToGraph](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N6) | 　ムービーグラフィックの動画の再生位置を得る |
| ○ | [GetMovieStateToGraph](https://dxlib.xsrv.jp/function/dxfunc_graph3.html#R14N5) | 　ムービーグラフィックの動画の再生状態を得る |

## マスク関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [CreateMaskScreen](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N1) | 　マスク画面を作成する |
| ○ | [DeleteMaskScreen](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N2) | 　マスク画面を削除する |
| ○ | [LoadMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N3) | 　マスクデータを画像ファイル(BMP.JPEG.PNG)から構築する |
| ○ | [LoadDivMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N4) | 　マスクデータを画像ファイル(BMP.JPEG.PNG)から分割構築する |
| ○ | [DrawMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N5) | 　マスクデータをマスク画面に描画する |
| ○ | [DrawFillMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N6) | 　指定のマスク画面領域を指定のマスクデータをタイル上に並べて埋める |
| ○ | [DeleteMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N7) | 　マスクデータを削除 |
| ○ | [InitMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N8) | 　マスクデータを初期化する |
| ○ | [FillMaskScreen](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N9) | 　マスク画面を指定の色で塗りつぶす |
| ○ | [SetUseMaskScreenFlag](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N10) | 　マスク画面の有効の有無を変更 |
| ○ | [MakeMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N11) | 　空のマスクデータの作成 |
| ○ | [GetMaskSize](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N12) | 　マスクデータの大きさを得る |
| ○ | [SetDataToMask](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N13) | 　マスクのデータをマスクデータ領域に転送する |
| ○ | [DrawMaskToDirectData](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N14) | 　マスクのデータをマスク画面に直接描画する |
| ○ | [DrawFillMaskToDirectData](https://dxlib.xsrv.jp/function/dxfunc_graph4.html#R16N15) | 　マスクのデータをタイル上に並べた形で直接マスク画面全体に描画する |

## 入力関係の関数

### ジョイパッド入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [GetJoypadNum](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N3) | 　ジョイパッドが接続されている数を取得する |
| ○ | [GetJoypadInputState](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N4) | 　ジョイパッドの入力状態を得る |
| ○ | [GetJoypadAnalogInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N24) | 　ジョイパッドのアナログ的なレバー入力情報を得る |
| ○ | [GetJoypadDirectInputState](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N34) | 　ジョイパッドのDirectInputから取得できる情報を得る |
| | [GetJoypadXInputState](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N35) | 　ジョイパッドのXInputから取得できる情報を得る |
| ○ | [SetJoypadDeadZone](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N37) | 　ジョイパッドの方向入力の無効範囲を設定する |
| | [StartJoypadVibration](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N30) | 　ジョイパッドの振動を開始する |
| | [StopJoypadVibration](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N31) | 　ジョイパッドの振動を停止する |

### マウス入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [SetMouseDispFlag](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N5) | 　マウスカーソルの表示設定フラグのセット |
| ○ | [GetMousePoint](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N6) | 　マウスカーソルの位置を取得する |
| | [SetMousePoint](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N7) | 　マウスカーソルの位置をセットする |
| ○ | [GetMouseInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N8) | 　マウスのボタンの状態を得る |
| ○ | [GetMouseInputLog2](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N40) | 　マウスのボタンが押されたり離されたりした履歴を取得する |
| ○ | [GetMouseWheelRotVol](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N32) | 　マウスホイールの回転量を得る |

### タッチパネル入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [GetTouchInputNum](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N38) | 　タッチされている箇所の数を取得する |
| ○ | [GetTouchInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N39) | 　タッチされている箇所の情報を取得する |

## キーボード入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [CheckHitKeyAll](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N1) | 　すべてのキーの押下状態を取得 |
| ○ | [CheckHitKey](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N2) | 　特定キーの入力状態を得る |
| ○ | [GetHitKeyStateAll](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N28) | 　キーボードのすべてのキーの押下状態を取得する |

### 半角文字入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [GetInputChar](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N25) | 　文字入力バッファに溜まった文字データから１文字取得する |
| | [GetInputCharWait](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N26) | 　文字入力バッファに溜まった文字データから１文字取得する、バッファになにも文字コードがない場合はキーが押されるまで待つ |
| | [ClearInputCharBuf](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N27) | 　文字入力バッファをクリアする |

### 日本語入力関連関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [KeyInputString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N9) | 　キーボードによる文字列の入力 |
| | [KeyInputSingleCharString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N10) | 　キーボードによる半角文字列のみの入力 |
| | [KeyInputNumber](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N11) | 　キーボードによる数値の入力 |
| | [SetKeyInputStringColor](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N12) | 　KeyInputString系 関数使用時の文字の各色を変更する |
| | [MakeKeyInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N13) | 　新しいキー入力データの作成 |
| | [DeleteKeyInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N14) | 　キー入力データの削除 |
| | [InitKeyInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N15) | 　すべてのキー入力データの削除 |
| | [SetActiveKeyInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N16) | 　指定のキー入力をアクティブにする |
| | [CheckKeyInput](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N17) | 　入力が終了しているか取得する |
| | [DrawKeyInputString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N18) | 　キー入力中データの描画 |
| | [DrawKeyInputModeString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N19) | 　入力モード文字列を描画する |
| | [SetKeyInputString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N20) | 　キー入力データに指定の文字列をセットする |
| | [SetKeyInputNumber](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N21) | 　キー入力データに指定の数値を文字に置き換えてセットする |
| | [GetKeyInputString](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N22) | 　入力データの文字列を取得する |
| | [GetKeyInputNumber](https://dxlib.xsrv.jp/function/dxfunc_input.html#R5N23) | 　入力データの文字列を数値として取得する |

## 音利用関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [PlaySoundFile](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N1) | 　音ファイルを再生する |
| ○ | [CheckSoundFile](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N2) | 　音ファイルが再生中か調べる |
| ○ | [StopSoundFile](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N3) | 　音ファイルの再生を止める |
| ○ | [LoadSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N4) | 　音ファイルをメモリに読みこむ |
| ○ | [PlaySoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N5) | 　メモリに読みこんだ音データを再生する |
| ○ | [CheckSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N6) | 　メモリに読みこんだ音データが再生中か調べる |
| ○ | [StopSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N7) | 　メモリに読み込んだ音データの再生を止める |
| ○ | [DeleteSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N8) | 　メモリに読みこんだ音データを削除する |
| ○ | [InitSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N9) | 　メモリに読みこんだ音データをすべて消去する |
| ○ | [ChangePanSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N10) | 　メモリに読みこんだ音データの再生にパンを設定する |
| ○ | [ChangeVolumeSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N11) | 　メモリに読みこんだ音データの再生にボリュームを設定する |
| ○ | [ChangeNextPlayPanSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N32) | 　メモリに読みこんだ音データの次の再生にのみ使用するパンを設定する |
| ○ | [ChangeNextPlayVolumeSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N33) | 　メモリに読みこんだ音データの次の再生にのみ使用するボリュームを設定する |
| ○ | [SetFrequencySoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N12) | 　メモリに読み込んだ音データの再生周波数を設定する |
| ○ | [SetLoopPosSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N13) | 　メモリに読み込んだ音データのループ位置を設定する |
| ○ | [SetLoopSamplePosSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N14) | 　メモリに読み込んだ音データのループ位置を設定する(サンプル位置指定) |
| ○ | [SetCurrentPositionSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N15) | 　メモリに読み込んだ音データの再生位置をサンプル単位で変更する |
| ○ | [DuplicateSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N16) | 　既にメモリに読み込んである音データを使用するサウンドハンドルを新たに作成する( 非ストリームサウンドのみ ) |
| ○ | [SetCreateSoundPitchRate](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N36) | 　作成するメモリに読み込んだ音データのピッチ( 音の長さを変えずに音程を変更する )レートを設定する |
| ○ | [SetCreateSoundTimeStretchRate](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N37) | 　作成するメモリに読み込んだ音データのタイムストレッチ( 音程を変えずに音の長さを変更する )レートを設定する |
| ○ | [Set3DPositionSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N17) | 　メモリに読み込んだ音データの３Ｄサウンド用の再生位置を設定する |
| ○ | [Set3DRadiusSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N18) | 　メモリに読み込んだ音データの３Ｄサウンド用の音が聞こえる距離を設定する |
| | [Set3DVelocitySoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N19) | 　メモリに読み込んだ音データの３Ｄサウンド用の移動速度を設定する |
| ○ | [SetNextPlay3DPositionSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N20) | 　メモリに読み込んだ音データの次の再生のみに使用する３Ｄサウンド用の再生位置を設定する |
| ○ | [SetNextPlay3DRadiusSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N21) | 　メモリに読み込んだ音データの次の再生のみに使用する３Ｄサウンド用の音が聞こえる距離を設定する |
| | [SetNextPlay3DVelocitySoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N22) | 　メモリに読み込んだ音データの次の再生のみに使用する３Ｄサウンド用の移動速度を設定する |
| | [Set3DReverbParamSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N23) | 　メモリに読み込んだ音データの３Ｄサウンド用のリバーブエフェクトパラメータを設定する |
| | [Set3DPresetReverbParamSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N24) | 　メモリに読み込んだ音データの３Ｄサウンド用のリバーブエフェクトパラメータをプリセットを使用して設定する |
| | [Get3DPresetReverbParamSoundMem](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N34) | 　３Ｄサウンド用のプリセットのリバーブエフェクトパラメータを取得する |
| | [Set3DReverbParamSoundMemAll](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N25) | 　全てのメモリに読み込んだ音データの３Ｄサウンド用のリバーブエフェクトパラメータを設定する |
| | [Set3DPresetReverbParamSoundMemAll](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N26) | 　全てのメモリに読み込んだ音データの３Ｄサウンド用のリバーブエフェクトパラメータをプリセットを使用して設定する |
| ○ | [SetCreate3DSoundFlag](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N27) | 　次に作成するメモリに読み込む音データを３Ｄサウンド用にするかどうかを設定する |
| | [SetEnableXAudioFlag](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N35) | 　サウンドの再生にXAudio2を使用するかどうかを設定する |
| ○ | [Set3DSoundOneMetre](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N28) | 　３Ｄ空間の１メートルに相当する距離を設定する |
| ○ | [Set3DSoundListenerPosAndFrontPos_UpVecY](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N29) | 　３Ｄサウンドのリスナーの位置とリスナーの前方位置を設定する |
| ○ | [Set3DSoundListenerPosAndFrontPosAndUpVec](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N30) | 　３Ｄサウンドのリスナーの位置とリスナーの前方位置とリスナーの上方向を設定する |
| | [Set3DSoundListenerVelocity](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R8N31) | 　３Ｄサウンドのリスナーの移動速度を設定する |

## 音楽再生関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [PlayMusic](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R9N1) | 　ＭＩＤＩ又はＭＰ３ファイルを演奏(再生)する |
| | [CheckMusic](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R9N2) | 　ＭＩＤＩ又はＭＰ３ファイルが演奏(再生)中かの情報を取得する |
| | [StopMusic](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R9N3) | 　ＭＩＤＩ又はＭＰ３ファイルの演奏(再生)停止 |
| | [SetVolumeMusic](https://dxlib.xsrv.jp/function/dxfunc_sound.html#R9N4) | 　ＭＩＤＩ又はＭＰ３ファイルの演奏(再生)の音量を設定する |

## ウエイト関係の関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [WaitTimer](https://dxlib.xsrv.jp/function/dxfunc_other.html#R6N1) | 　指定の時間だけ処理をとめる |
| | [WaitVSync](https://dxlib.xsrv.jp/function/dxfunc_other.html#R6N2) | 　ディスプレイの垂直同期信号を指定回数待つ |
| ○ | [WaitKey](https://dxlib.xsrv.jp/function/dxfunc_other.html#R6N3) | 　キーの入力待ち |

## 時間関係の関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [GetNowCount](https://dxlib.xsrv.jp/function/dxfunc_other.html#R7N1) | 　ミリ秒単位の精度を持つカウンタの現在値を得る |
| ○ | [GetNowHiPerformanceCount](https://dxlib.xsrv.jp/function/dxfunc_other.html#R7N2) | 　GetNowCountの高精度バージョン |
| ○ | [GetDateTime](https://dxlib.xsrv.jp/function/dxfunc_other.html#R7N3) | 　現在時刻を取得する |

## 乱数取得関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [GetRand](https://dxlib.xsrv.jp/function/dxfunc_other.html#R10N1) | 　乱数を取得する |
| ○ | [SRand](https://dxlib.xsrv.jp/function/dxfunc_other.html#R10N2) | 　乱数の初期値を設定する |

## ウインドウモード関係

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [ChangeWindowMode](https://dxlib.xsrv.jp/function/dxfunc_other.html#R11N1) | 　ウインドウモード・フルスクリーンモードの変更を行う |
| | [SetMainWindowText](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N13) | 　ウインドウのタイトルを変更する |
| | [SetWindowIconID](https://dxlib.xsrv.jp/function/dxfunc_other.html#R11N2) | 　ウインドウのアイコンを変更する |
| | [SetWindowSizeChangeEnableFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R11N3) | 　ウインドウモードの時にウインドウのサイズを自由に変更出来るようにするかどうかを設定する |
| | [SetWindowSizeExtendRate](https://dxlib.xsrv.jp/function/dxfunc_other.html#R11N4) | 　ウインドウモードの時のウインドウの大きさと描画画面の大きさの比率を設定する |

## 通信関係

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [ConnectNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N1) | 　他のマシンに接続する |
| | [CloseNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N2) | 　接続を終了する |
| | [PreparationListenNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N3) | 　接続を受け付けられる状態にする |
| | [StopListenNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N4) | 　接続を受け付けている状態を解除する |
| | [NetWorkSend](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N5) | 　データを送信する |
| | [GetNetWorkDataLength](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N6) | 　受信データ一時記憶バッファに溜まっているデータの量を得る |
| | [GetNetWorkSendDataLength](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N7) | 　未送信のデータの量を得る |
| | [NetWorkRecv](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N8) | 　受信データ一時記憶バッファに溜まっているデータを取得する |
| | [NetWorkRecvToPeek](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N9) | 　受信したデータを読み込む、読み込んだデータはバッファから削除されない |
| | [GetNewAcceptNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N10) | 　新たに確立した接続を示すネットワークハンドルを得る |
| | [GetLostNetWork](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N11) | 　新たに破棄された接続を示すネットワークハンドルを得る |
| | [GetNetWorkAcceptState](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N12) | 　接続状態を取得する |
| | [GetNetWorkIP](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N13) | 　接続先のＩＰアドレスを得る |
| | [MakeUDPSocket](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N14) | 　ＵＤＰを使用して通信するためのソケットを作成する |
| | [DeleteUDPSocket](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N15) | 　ＵＤＰを使用して通信するためのソケットを削除する |
| | [NetWorkSendUDP](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N16) | 　ＵＤＰを使用して他のマシンにデータを送信する |
| | [NetWorkRecvUDP](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N17) | 　ＵＤＰを使用して他のマシンからのデータを受信する |
| | [CheckNetWorkRecvUDP](https://dxlib.xsrv.jp/function/dxfunc_other.html#R13N18) | 　ＵＤＰを使用した他のマシンから受信データがあるかどうかを取得する |

## ファイル読み込み関係

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [FileRead_open](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N1) | 　ファイルを開く |
| ○ | [FileRead_size](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N2) | 　ファイルのサイズを得る |
| ○ | [FileRead_close](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N3) | 　ファイルを閉じる |
| ○ | [FileRead_tell](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N4) | 　ファイルポインタの位置を得る |
| ○ | [FileRead_seek](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N5) | 　ファイルポインタの位置を変更する |
| ○ | [FileRead_read](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N6) | 　ファイルからデータを読み込む |
| ○ | [FileRead_eof](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N7) | 　ファイルの終端かどうかを調べる |
| ○ | [FileRead_gets](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N8) | 　ファイルから一行読み出す |
| ○ | [FileRead_getc](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N9) | 　ファイルから一文字読み出す |
| ○ | [FileRead_scanf](https://dxlib.xsrv.jp/function/dxfunc_other.html#R19N10) | 　ファイルから書式付きデータを読み出す |

## ドット単位で画像にアクセスしたい関係

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [LoadSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N1) | 　ＣＰＵで扱うイメージの読み込み |
| ○ | [LoadARGB8ColorSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N20) | 　ＣＰＵで扱うイメージの読み込み( RGBA8 カラーに変換 ) |
| ○ | [LoadXRGB8ColorSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N21) | 　ＣＰＵで扱うイメージの読み込み( XGBA8 カラーに変換 ) |
| ○ | [LoadSoftImageToMem](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N2) | 　ＣＰＵで扱うイメージのメモリからの読み込み |
| ○ | [LoadARGB8ColorSoftImageToMem](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N22) | 　ＣＰＵで扱うイメージのメモリからの読み込み( RGBA8 カラーに変換 ) |
| ○ | [LoadXRGB8ColorSoftImageToMem](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N23) | 　ＣＰＵで扱うイメージのメモリからの読み込み( XGBA8 カラーに変換 ) |
| ○ | [MakeARGB8ColorSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N3) | 　ＣＰＵで扱うイメージの作成( RGBA8 カラー ) |
| ○ | [MakeXRGB8ColorSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N18) | 　ＣＰＵで扱うイメージの作成( XRGB8 カラー ) |
| ○ | [MakePAL8ColorSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N4) | 　ＣＰＵで扱うイメージの作成( パレット２５６色 カラー ) |
| ○ | [DeleteSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N5) | 　ＣＰＵで扱うイメージの解放 |
| ○ | [InitSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N19) | 　ＣＰＵで扱うイメージを全て解放 |
| ○ | [GetSoftImageSize](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N6) | 　ＣＰＵで扱うイメージのサイズを取得する |
| ○ | [FillSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N7) | 　ＣＰＵで扱うイメージを指定色で塗りつぶす(各色要素は０～２５５) |
| ○ | [SetPaletteSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N9) | 　ＣＰＵで扱うイメージのパレットをセットする(各色要素は０～２５５) |
| ○ | [GetPaletteSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N8) | 　ＣＰＵで扱うイメージのパレットを取得する(各色要素は０～２５５) |
| ○ | [DrawPixelPalCodeSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N10) | 　ＣＰＵで扱うイメージの指定座標にドットを描画する(パレット画像用、有効値は０～２５５) |
| ○ | [GetPixelPalCodeSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N11) | 　ＣＰＵで扱うイメージの指定座標の色コードを取得する(パレット画像用、戻り値は０～２５５) |
| ○ | [DrawPixelSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N12) | 　ＣＰＵで扱うイメージの指定座標にドットを描画する(各色要素は０～２５５) |
| ○ | [GetPixelSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N13) | 　ＣＰＵで扱うイメージの指定座標の色を取得する(各色要素は０～２５５) |
| ○ | [BltSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N14) | 　ＣＰＵで扱うイメージを別のイメージ上に転送する |
| ○ | [DrawSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N15) | 　ＣＰＵで扱うイメージを画面に描画する |
| ○ | [CreateGraphFromSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N16) | 　ＣＰＵで扱うイメージからグラフィックハンドルを作成する |
| ○ | [CreateDivGraphFromSoftImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R20N17) | 　ＣＰＵで扱うイメージから分割グラフィックハンドルを作成する |

## 非同期読み込み関係

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [SetUseASyncLoadFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R21N1) | 　非同期読み込みを行うかどうかを設定する |
| ○ | [CheckHandleASyncLoad](https://dxlib.xsrv.jp/function/dxfunc_other.html#R21N2) | 　ハンドルが非同期読み込み中かどうかを取得する |
| ○ | [GetASyncLoadNum](https://dxlib.xsrv.jp/function/dxfunc_other.html#R21N3) | 　行っている非同期読み込みの数を取得する |

## 文字関係関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| ○ | [SetUseCharCodeFormat](https://dxlib.xsrv.jp/function/dxfunc_other.html#R22N1) | 　文字列の引数の文字コードを設定する |
| ○ | [GetCharBytes](https://dxlib.xsrv.jp/function/dxfunc_other.html#R22N2) | 　文字列の先頭の文字のバイト数を取得する |

## マイナー関数

| 対応 | 関数名 | 関数の説明 |
|:--|:--|:--|
| | [SetAlwaysRunFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N22) | 　ウインドウがアクティブではない状態でも処理を続行するか、フラグをセットする |
| ○ | [SetOutApplicationLogValidFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N14) | 　ログ出力を行うか否かのセット |
| ○ | [SetUseDXArchiveFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N30) | 　ＤＸアーカイブファイルの読み込み機能を使うかどうかを設定する |
| ○ | [SetDXArchiveExtension](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N31) | 　検索するＤＸアーカイブファイルの拡張子を変更する |
| ○ | [SetDXArchiveKeyString](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N32) | 　ＤＸアーカイブファイルの鍵文字列を設定する |
| | [SetEmulation320x240](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N37) | 　６４０ｘ４８０の画面で３２０ｘ２４０の画面解像度にするかどうかのフラグをセットする |
| | [SetUse3DFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N1) | 　３Ｄ機能を使うか、のフラグをセット |
| | [SetWaitVSyncFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N5) | 　ScreenFlip関数実行時にＣＲＴの垂直同期信号待ちをするかのフラグセット |
| ○ | [SetDrawCustomBlendMode](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N39) | 　描画の際のブレンドモードを詳細に設定する |
| ○ | [SetUseDivGraphFlag](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N24) | 　必要ならグラフィックの分割を行うか否かを設定する |
| | [LoadPauseGraph](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N12) | 　フォーカスが他のソフトに移っているときにバックグラウンドに表示するグラフィックを設定する |
| ○ | [ScreenCopy](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N19) | 　裏画面の内容を表画面にコピーする |
| ○ | [GetColorBitDepth](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N6) | 　画面の色ビット数を得る |
| ○ | [SaveDrawScreen](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N11) | 　現在描画対象になっている画面をＢＭＰ形式で保存する |
| | [EnumFontName](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N20) | 　使用可能なフォントの名前を列挙する |
| ○ | [DrawVString](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N8) | 　文字列を縦に描画する |
| ○ | [DrawVStringToHandle](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N9) | 　フォントハンドルを使用して文字列を縦に描画する |
| ○ | [CreateGraphFromMem](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N26) | 　メモリ上の画像ファイルイメージからグラフィックハンドルを作成する |
| ○ | [ReCreateGraphFromMem](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N34) | 　メモリ上の画像ファイルイメージから既存のグラフィックハンドルにデータを転送する |
| ○ | [ReloadFileGraphAll](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N35) | 　画像ファイルから作成したグラフィックハンドルに再度画像ファイルから画像を読み込む |
| ○ | [SetRestoreGraphCallback](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N33) | 　グラフィックハンドル復元関数を登録する |
| ○ | [SetCreateSoundDataType](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N25) | 　作成する音データの再生形式を設定する |
| ○ | [LoadSoundMemByMemImage](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N27) | 　メモリ上の音ファイルイメージからサウンドハンドルを作成する |
| | [SelectMidiMode](https://dxlib.xsrv.jp/function/dxfunc_other.html#R15N21) | 　ＭＩＤＩの演奏形態をセットする |
