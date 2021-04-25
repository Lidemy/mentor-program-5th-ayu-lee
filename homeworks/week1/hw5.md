## Week1-hw5 簡答題

#### A. 請解釋後端與前端的差異

前端 front-end 後端 back-end ，用舞台劇來舉例可能類似：觀眾（使用者）- 演員（前端，穿戲服說台詞）- 幕後人員（後端，遞送道具確認上場順序）。

前端是整體**看得到的呈現**，包含內容、視覺、介面、與使用者的互動等，後端的話則是這一切要完成時**看不到的部分**，連線遠端的伺服器、資料庫的抓取運算、資料回傳等。而這關鍵的區別位置（舞台帷幕）應該就是在**Server 網路伺服器**，伺服器作為載具在使用者與其他伺服器之間收發資料，來完成其所欲達成之事。簡單理解的話：伺服器的介面呈現（網頁：內容、樣式、互動）屬於前端，伺服器在電腦網路中的運算回傳等（系統架構）屬於後端。

---

#### B. Google 首頁搜尋框打上：JavaScript 並按下 Enter，從這一刻開始到看到搜尋結果為止發生在背後的事情

動作之前：使用電腦OS 作業系統中的網頁瀏覽器 chorme，網路卡連接到網路。輸入網址  www.google.com ，透過DNS（Domain Name System）轉換成 google IP位址（主機位址）後，連上 google 伺服器。搜尋欄上鍵入" Java Script" 。

1. " Java Script " 字串被上傳到 Server，Server 收到 request
2. Server 把字串交給資料庫 Database 抓取，查詢到" Java Script " 。
3.  資料庫 response 回傳結果資料到 Server。
4. Server response 回傳資料到我的 IP位址 瀏覽器。
5. 瀏覽器 透過資料，藉由 html （檔案內容）、CSS （樣式視覺）、JavaScript （功能操作）等呈現出字串 Java Script 搜尋到的相關資料。

***

#### C. 3 個「課程沒有提到」的 command line 指令並且說明功用

`exit`  關閉視窗 （我沒看到這個指令前，都是直接按叉叉 XD）

`control+c`  取消目前指令（發現有點卡卡當住的時候可以用）

`Control+z`  中斷目前指令

`history` 可以顯示之前輸入的指令有哪些

`;` 分隔指令組成一行指令，例：`pwd ; ls`

`host` 查詢IP位址，例：`host google.com` 

`ping` 發送 echo request 到指定的位址 （很像跟網路有關，但用法內容說明我看不懂XD）