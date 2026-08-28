MapleAuto Rebuild 彩色圖像重連素材
==================================

程式使用目前 Windows 使用者已登入的 Edge，不建立專用設定檔，也不使用 Selenium。
所有模板皆使用彩色 BGR 比對，不轉灰階；建議 Windows 顯示比例與 Edge 縮放皆為 100%。

流程：
disconnect_confirm（確認是斷線訊息）→ disconnect_confirm_button（點擊確認，最多重試 3 次）
→ web_launch_game → web_gama_pass → web_allowed_account
→ web_character → web_continue → game_server
→ 隨機 game_channel_03／05／10／11／17
→ game_enterchannel → game_start

分流模板檔名：
game_channel_03.png（為相容舊版，也接受既有 game_channel.png）
game_channel_05.png
game_channel_10.png
game_channel_11.png
game_channel_17.png

每次登入會把五個分流隨機排序。若候選分流無法進入，程式會按 Enter
關閉可能出現的提示後，依本次隨機順序嘗試下一個。

自動重連前若任務正在執行，登入後必須連續三次同時確認小地圖與玩家位置，
才會恢復原路線；手動登入測試只會進入遊戲，不會自行開始路線。

web_forbidden_account 是安全排除模板。只有同時辨識到允許與禁止帳號列、且兩者區域
不重疊時才會點擊 a****2@gmail.com；n****0@gmail.com 永遠不會被點擊。

只有確認舊遊戲視窗已關閉後才會進入網站流程。找不到確認按鈕或點擊後 20 秒視窗
仍未關閉時會停止重連並通知，不會直接開啟第二個遊戲。
