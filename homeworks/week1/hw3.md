## Week1-hw3 教你朋友 CLI

---

#### 介紹CLI

CLI 是 **command line** 的簡寫，相對於 **GUI  (graphic user interface) 圖形化操作介面**，它是使用純文字方式與電腦 『 溝通 』下指令。完全不會使用程式語言的人（例如：我）還是可以每天用電腦工作，這是因為指令被設定成了各種圖像等直觀的操作介面，例如：執行某個繪圖軟體，直接點擊畫筆，使用滑鼠畫圖並直接顯示出來（而不是使用鍵盤對電腦打顏色代碼與輸入每個落筆的座標等）這就是圖形化操作介面。CLI 則反之，使電腦運作依賴的是每個敲打出的單字（指令）。而執行 command line ，首先要確認使用的電腦是什麼系統（ windows - 命令提示字元 cmd.exe／mac - 終端機 terminal.app 等）加裝對應的應用程式。安裝好後，就可以直接開始練習啦！

---

#### h0w哥的目標

###### 用 command line 建立一個叫做 wifi 的資料夾，並且在裡面建立一個叫 afu.js 的檔案

* 練習基本指令：

<font size=4>`pwd`</font>  print working directory 顯示目前所在位置 
<font size=4>`cd ..`</font>  change directory  變更所在位置（資料夾）// .. 代表回到上一層 
<font size=4>`ls -al`</font>  list 顯示所在位置內部文件檔案 //（可使用『 - 』接續各種參數，例：al 顯示包含隱藏的所有檔案）
<font size=4>`touch`</font>  **a.**改變檔案最後修改時間  **b.**新增檔案

<font size=4>`mkdir`</font>  make directory  新增資料夾

<font size=4>`rm -r`</font> remove 刪除檔案 （刪除資料夾時需要使用指令 -r 或 rmdir // 參數 -f 為強制刪除，要小心使用）

<font size=4>`rmdir`</font> remove directory 刪除資料夾

<font size=4>`mv`</font> move **a.**移動檔案位置  **b.**檔案重新命名（/絕對位置，根目錄 ； ~相對位置）
<font size=4>`cp`</font> copy 複製檔案（複製資料夾需要使用參數-r： `cp -r 資料夾名稱`
<font size=4>`man`</font> manual 使用手冊
<font size=4>`clear`</font> 清空畫面
<font size=4>`cat`</font> catenate連接 **a.**連接檔案 **b.**只放一個檔案參數，會顯示檔案內部內容，例如：`cat happy.txt`
<font size=4>`vim`</font>  進入檔案內部的文字編輯器 （使用較不直觀） 
  有不同模式： i - insert 插入模式，可打字  // esc - escape 普通模式，可插入複製貼上，但不能打字
  離開vim時需使用`shift:q`  // 存檔離開`shift:wq` (write quit)  // 有更動但不存檔離開 `shift:!q`
<font size=4>`open`</font> 開啟檔案
<font size=4>`echo`</font> 印出字串 例：`echo "123"`（印出123）//  `echo "hello" > hw.txt`（寫入hello到文件hw.txt）
<font size=4>`grep`</font> 抓關鍵字 `grep keyword 檔名`
<font size=4>`wget`</font> 下載檔案 ` wget _網址或圖片網址_`
<font size=4>`curl`</font> 送出request `curl _API網址_` 會show出網站回傳內容？可以拿來測試網站？

<font size=4>`>`</font> redirection 重新導向 input output（後導入的內容會覆蓋前面內容）`ls -al > list-result` ls -al輸出的內容導入到名為 list-result 的檔案裡

<font size=4>`>>`</font> append 新增導向 （後導入的內容新增於前面內容後、接續於內容後不會覆蓋）

<font size=4>`|`</font> pipe `左邊的輸出｜(左邊輸出)右邊的輸入` 例：`cat hello | grep o > result`  印出hello的內容，內容中抓取 字母 o ，並輸出至檔案 result

---

#### 練習好基本指令，h0w哥開始步驟

1. 叫出 terminal
2. `pwd` （確認目前工作位置）

3. `cd desktop`（移動位置到桌面）
4. `pwd`（確認自己已成功移動）
5. `mkdir wifi`（建立一個名稱『 wifi 』的資料夾）
6. `cd wifi`（移動到資料夾裡面）
7. `touch afu.js`（新增一個aft.js的檔案）
8. `ls`（列出 wifi 資料內檔案）
9. 看見出現 afu.js ，成功！想再確認，可以去桌面點擊看看 wifi 資料夾