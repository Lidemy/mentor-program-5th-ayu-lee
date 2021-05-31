## Week1-hw5 簡答題

#### A. 請解釋後端與前端的差異

- 前端 front-end（餐廳外場，接受點餐，擺盤上菜）：接受使用者指令並呈現網頁內容。
  前端是整體看得到的呈現，包含內容、視覺與使用者的互動等。而主要會運用到的三個工具分別為：HTML （網站架構、資訊內容）／CSS（外型樣式）／ JavaScript（使用程式語言，處理網站上*需要邏輯判斷*的功能）。

- 後端 back-end （餐廳後場，儲存食材、製作餐點）：處理指令並提供內容。屬於看不到的部分，包含 Server 伺服器運作、Database 資料庫的抓取運算、資料回傳等。

---

#### B. Google 首頁搜尋框打上：JavaScript 並按下 Enter，從這一刻開始到看到搜尋結果為止發生在背後的事情

動作之前：
使用電腦 OS 作業系統中的網頁瀏覽器 chorme，網路卡連接到網路。（瀏覽器向伺服器送出 HTTP 訊息，請求伺服器向用戶端傳送網站複本）輸入網址  www.google.com ，會先透過 DNS（Domain Name System）轉換成 google IP 位址（主機位址）後，用戶端連上 google 伺服器。

1. 使用者透過瀏覽器送出搜尋內容（請求） "JavaScript" 到 google Server，Server 收到 request。（用戶端與伺服器之間，請求訊息與其他資訊，會使用 TCP/IP 在網路連線間傳送）。
2. Server 從資料庫 Database 抓取，查詢到" Java Script "相關資料 。
3. 資料庫回傳 response 資料到 Server。
4. Server 回傳 response 資料封包到用戶端瀏覽器。
5. 瀏覽器 解讀資料，藉由 HTML（檔案內容）、CSS （樣式視覺）、JavaScript （功能操作）等呈現出 "Java Script" 搜尋到的相關內容。

***

#### C. 3 個「課程沒有提到」的 command line 指令並且說明功用

`exit`  離開目前狀態 

`control+c`  取消目前指令（發現有點卡卡當住的時候可以用）

`control+z`  中斷目前指令

`history` 可以顯示之前輸入的指令有哪些

`;` 分隔指令組成一行指令，例：`pwd ; ls`

`host` 查詢IP位址，例：`host google.com` 

`ping` 發送 echo request 到指定的位址 （很像跟網路有關，但用法內容說明我看不懂XD）