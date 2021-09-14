---
layout: page
title: オプションとパラメータ - win-vind
nav: オプションとパラメータ
disable_anchors: true
translation: ja
translators: pit-ray
version: 4.0.1
show_in_menu: false
---

## パラメータと初期値

|ID|型|初期値|備考|
|:---:|:---:|:---:|:---|
|`arrangewin_ignore`|str||ウィンドウの整列で無視する実行ファイル名のリスト。例えば、rainmeterとgvimを整列対象から外したい場合、`set arrangewin_ignore = rainmeter, gvim`のように書きます。名前は拡張子なしの実行ファイル名です。|
|`autofocus_textarea`|bool|false|**Editor Normalモード**に遷移したとき、自動的にマウスカーソルに最も近いテキストエリアを選択します。|
|`autotrack_popup`|bool|false|Windowsの標準オプションのうちの一つです。例えば、**このファイルをゴミ箱に移動しますか?**と表示されたときに、自動的にポップアップウィンドウへカーソルを移動させます。|
|`blockstylecaret_mode`|str|solid|ブロックスタイルのキャレットのモード。サイズ固定の`solid`モードと選択による疑似的な`flex`モードがあります。|
|`blockstylecaret_width`|num|15|solidモードのブロックスタイルキャレットの幅|
|`blockstylecaret`|bool|false|ブロックスタイルのキャレット|
|`charcache`|bool|false|`x`や`X`コマンドの時使われる1文字用の小さなキャッシュ。有効にすると、その都度クリップボードが開かれ、Vimと同じ動作になりますが、パフォーマンスが少し低下します。|
|`cmd_bgcolor`|str|323232|仮想コマンドラインの背景色 (#は任意)|
|`cmd_fadeout`|num|5|仮想コマンドラインのフェードアウト時間(秒)。コマンドラインを消えないようにするには、この値を十分大きなものにしてください。|
|`cmd_fontcolor`|str|c8c8c8|仮想コマンドラインの文字色 (#は任意)|
|`cmd_fontextra`|num|1|仮想コマンドラインの水平方向の文字間隔|
|`cmd_fontname`|str|Consolas|仮想コマンドラインのフォント名。空の文字列の場合には、システムフォントが利用されます。|
|`cmd_fontsize`|num|23|仮想コマンドラインの文字サイズ|
|`cmd_fontweight`|num|400|仮想コマンドラインの文字の太さ。(最大値: 1000)|
|`cmd_maxchar`|num|32|仮想コマンドラインの一行あたりの最大文字数|
|`cmd_maxhist`|num|10|仮想コマンドラインで保持する履歴の最大数|
|`cmd_roughpos`|str|LowerMid|仮想コマンドラインの大まかな位置。`UpperLeft`, `UpperMid`, `UpperRight`, `MidLeft`, `Center`, `MidRight`, `LowerLeft`, `LowerMid`, `LowerRight`のうちのどれかを指定してください。|
|`cmd_xmargin`|num|32|`cmd_roughpos`で大まかな位置を決め、ピクセル単位で水平方向の微調整を行います。|
|`cmd_ymargin`|num|64|`cmd_roughpos`で大まかな位置を決め、ピクセル単位で垂直方向の微調整を行います。|
|`cursor_accel`|num|95|マウスカーソルの等加速度運動におけるピクセルレベルの加速度。|
|`cursor_maxv`|num|12|マウスカーソルの最大速度。|
|`cursor_tweight`|num|250|マウスカーソルの等加速度運動における時間のスケーリング値。|
|`dedicate_to_window`|bool|false|If **Dedicate to One window** enables, you can select one window with Enable Targeting function. In this case, it makes the mode automatically switch to Editor Normal Mode on the targeting window. When the foreground window change to another, it makes the mode switch to Insert Mode. The targeting becomes disable with Disable Targeting function. In other words, this feature transforms some normal editors to fake Vim. The computing cost is so small.|
|`easyclick_bgcolor`|str|323232|EasyClickのヒントの背景色 (#は任意)|
|`easyclick_colordecay`|num|100|EasyClickでマッチングしているヒントの色減衰値 (0 ~ 255)|
|`easyclick_fontcolor`|str|c8c8c8|EasyClickのヒントの文字色 (#は任意)
|`easyclick_fontname`|str|Arial|EasyClickのヒントのフォント名|
|`easyclick_fontsize`|num|14|EasyClickのヒントの文字サイズ|
|`easyclick_fontweight`|num|500|EasyClickのヒントの文字の太さ。(最大値: 1000)|
|`gui_fontname`|str|Segoe UI|GUIのフォント名。空文字の場合には、システムフォントが利用されます。|
|`gui_fontsize`|num|11|GUIのフォントサイズ|
|`hscroll_pageratio`|num|0.125|The ratio of one page to the screen width to determine the amount of scrolling movement as a page.
|`hscroll_speed`|num|10|Horizontal scrolling speed of the mouse wheel.|
|`icon_style`|str|resources/icon32_dark.ico|Style of the icon to be displayed on the taskbar. By default, **Dark** and **Light** styles are available. The former is `resources/icon32_dark.ico` and the latter is `resouces/icon32_light.ico`. By the way, you can use any tasktray icon you like as long as it is in `.ico` format and **32x32**.|
|`initmode`|str|i|win-vindの初期モード。値はモード接頭辞です。|
|`jump_margin`|num|10|A margin in pixels to prevent jumping off the screen when jumping to the edge of the screen using `jump_cursor_to_left`, etc.|
|`keybrd_layout`|str||Keyboard layout kmp file referenced by `jump_cursor_with_keybrd_layout`. By default, only **US (101/102)** or **JP (106/109)** layouts are supported. If your keyboard is not the right one, please create your own kmp file and use its path as the value. If you leave the value empty, the KMP file will be selected automatically. Also, if you like, you can share the keyboard you created with a pull request to the `default_config` directory.|
|`shell_startupdir`|str||The current directory where commands (e.g. `:shell`, `:terminal`, `:!`) will be executed. For these commands, the current directory is the directory if there is Exeplorer, or the user directory otherwise. If this option is not empty, then the current directory is fixed to a value directory.|
|`shell`|str|cmd|Name of the shell to use for `:!` commands|
|`shellcmdflag`|str|-c|Flag passed to the shell to execute `:!` commands|
|`suppress_for_vim`|bool|false|It makes the mode of win-vind automatically switch to **Resident Mode** on the applications included the strings called **VIM** in an executable file name. Thus, it allows us to smoothly move from win-vind having the same key-bindings as Vim to Vim applications.|
|`uiacachebuild_lifetime`|num|1500|Cache lifetime (ms). A high value reduces the computational cost, but decreases the reliability of the cache. A low value increases the computational cost due to frequent cache creation, but guarantees reliability.|
|`uiacachebuild_staybegin`|num|500|The time between when the mouse cursor stops moving and when it starts to build a cache. In order to reduce unnecessary computational cost, it is desirable not to create a cache when there is no operation. Therefore, it should be updated only immediately after the mouse stops. The value of this option is the time(ms) that the mouse cursor is considered to be stopped. Please refer to [appendix](#overview-of-stay-range-in-uiacachebuild)|
|`uiacachebuild_stayend`|num|2000|In order to reduce unnecessary computational cost, it is desirable not to create a cache when there is no operation. The value of this option is the time(ms) between the time the cursor stops moving and the time it stops creating a cache. Please refer to appendix [appendix](#overview-of-stay-range-in-uiacachebuild)|
|`uiacachebuild`|bool|false|EasyClick and `autofocus_textarea` are slow because they scan the UI object after being called. If this option is enabled, scanning is done asynchronously and cache is used as a result. Using the cache is 30 times faster than scanning linearly, but the location information, etc. may not always be correct.|
|`vcmdline`|bool|true|仮想コマンドライン|
|`vscroll_pageratio`|num|0.125|The ratio of one page to the screen height to determine the amount of scrolling movement as a page.
|`vscroll_speed`|num|30|Vertical scrolling speed of the mouse wheel.|
|`window_accel`|num|95|Pixel-level acceleration in the constatnt acceleration motion of the window in winresizer.|
|`window_hdelta`|num|100|Window Width delta for resizing|
|`window_maxv`|num|12|Maximum velocity of the window in winresizer.|
|`window_tweight`|num|250|A weight for scaling the time of constant acceleration motion of the window in winresizer.|
|`window_vdelta`|num|100|Window height delta for resizing|
|`winresizer_initmode`|num|0|window resizerの初期モード([0]: Resize, [1]: Move, [2]: Focus)|


## Appendix

### Overview of stay range in `uiacachebuild`
<p align="center">
<img src="{{ site.url }}/imgs/uiacachebuild_stay.png" width=600>  
<p align="center">uiacachebuild_staybegin and uiacachebuild_stayend overview</p>
</p>


<br>
<br>
<br>
<br>
