失落的國度 mudlet 地圖

使用方法:
1. 下載和安裝 mudlet https://www.mudlet.org/zh/
2. 選擇設定檔進行連線. 新建. 服務器地址: doom.twmuds.com. 端口: 4000. 連接
![mudlet1](https://github.com/user-attachments/assets/46ffbe95-b37c-46a4-a83a-13231bb70bc9)
3. 選項. 偏好設定. 資料編碼: Big5-ETen(台灣)
![mudlet2](https://github.com/user-attachments/assets/f93f14f2-270c-4001-ae9f-962358c681bf)
4. 工具列. Package.
![mudlet3](https://github.com/user-attachments/assets/89998853-b1ef-4b34-a6fc-c16b88716cff)
5. 移除generic_mapper

![mudlet4](https://github.com/user-attachments/assets/32b7aa45-525a-45d8-b09a-243c33818d65)

6. 安裝新的軟件包. 選擇上面下載的 doom mapper.mpackage

![mudlet5](https://github.com/user-attachments/assets/59454ba4-a6fc-46a4-8a75-4946ec0fb8dc)

7. 回到主視窗. 選項. 偏好設定. 地圖工具. 載入其他地圖. 選擇上面下載的doom map.dat
![mudlet6](https://github.com/user-attachments/assets/b190d63b-5677-4e1b-864d-5d36f89eb42a)
8. 回到主視窗. 角色登入遊戲後輸入 "set prompt ppt$Hppt" . 理論上這在登入時會自動輸入,這裡是預防萬一. 這把prompt改成mapper好截取的格式.
![mudlet7](https://github.com/user-attachments/assets/781f5373-0195-4f82-ad0d-c2bd4de6cb3b)
9. 回到主視窗. 工具列. 地圖
![mudlet8](https://github.com/user-attachments/assets/26ba2f38-de2a-4b18-8304-87490d8dc959)
10. 在遊戲裡輸入 "look" 然後 "ll"(兩個L) 來定位在地圖上的位置
![mudlet9](https://github.com/user-attachments/assets/b00b4721-5ef7-44f9-b891-cb311c1a5932)
11. 完成.

-需要地圖找到現在位置, 先"look,"再輸入 "ll" (兩個L) 或 "lll"(三個L). 後者是忽略房間出口的搜尋.

-要創造地圖的時候,輸入"mc" (map create).

-不要創造地圖的時候,輸入"mf" (map follow).

-要創造特殊出口,輸入"spe <room id> <alias> <special command>." 如果有多個 special commands, 寫 script:sendAll(<speciall commands separated by commas>). 例如: spe 2930 n script:sendAll("move tree","n").

-要取消特殊出口的alias,先讓地圖定位在該房間,然後輸入 "data del."

-地圖壞掉沒辦法接受移動指令時, 輸入"mo" (map off). 移動了之後再 "mf."

-在編輯地圖時,如果選擇的房間有重疊,選擇的房間會呈現黃色的標靶符號. 此時可以在左上角的視窗來篩選房間. 如果要把重疊的房間合併,先把玩家位置定位在該房間,然後輸入"merge rooms."

![mudlet10](https://github.com/user-attachments/assets/5d0b9b3a-5f27-4d30-a696-131b1b40c076)

-增加門: "add door <direction> [none|open|closed|locked] [yes|no]"

-要創造一個由特殊出口到的新的房間,先輸入"mf," 然後從目前的房間走到新的房間,輸入"mc <direction>." 這會在目前房間的指定方向創造這個新的房間.然後用"spe <alias> <special command>"來創造到前一個房間的特殊出口.依此類推.

-鐘鼓森林的房間沒有名稱,必須輸入"nameless on"才可以使用地圖. 離開以後輸入"nameless off."

-房間名稱會包含名稱加第一行敘述.由"_"分開. 房間的資訊會存在getRoomUserData() 的 "roomName," "description," "descriptionFirstLine," 和 "note."

-搜尋房間: "rs <關鍵詞>" (room search).

-搜尋物品 "rso <物品名稱>" (room search object)

-搜尋物品筆記 "rson <lua regex>"

-房間筆記: "rr <room id> <note>" 或者 "rr <note>" 或者 "rr." 刪除用 "rn del."

-物品筆記: 用滑鼠按物品旁邊的 add 把他存到地圖檔的room user data. 用滑鼠按 note 然後用 "rr <note>"可以寫物品筆記. 按下物品或房間的筆記會把它複製到剪貼簿上.

-撞隱藏出口: "td" 或者 "tdd."

-隨機走路: "randomwalk <delay> <stopping prompt>." Delay is in seconds. 輸入 "stop" 來停止 random walk.

-在地圖的房間上雙擊滑鼠左鍵可以快走.

-在地圖編輯模式下用滑鼠拖動地圖要按住Alt鍵.

-失落的國度有機器人檢查. 需要定期輸入"active 驗證碼."

-覺得字體太大的話,到選項, 偏好設定,顯示設定,字體改成細明體,大小12.

-我只是失落的國度的新手.地圖完成度可能不到2/3.

-我是mudlet的新手.這個package是根據generic mapper隨便改寫的.

-感謝Longinus的幫助.

https://doomoflostkingdoms.blogspot.com/
