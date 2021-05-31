## Week1-hw1 交作業流程

---

本課程使用 **GitHub** 上傳作業，以下為大略使用流程

1. 取得 Lidemy 第五期課程為個人開設的 repository 專案（使用邀請開通連結）。

2. 電腦上開啟 terminal 使用 CLI 語法 移動至欲存放專案的資料夾 downloads/lidemy。

3. 進入第一步的連結並複製專案網址，`git clone https://github.com/Lidemy/mentor-program-5th-ayu-lee.git`  完成個人電腦上（ Local 端）的更新。

4. `cd ~/downloads/lidemy/mentor-program-5th-ayu-lee`  ,  `ls` 查看目前專案資料夾內的內容檔案有哪些；`git log `查看目前 git 版本紀錄。

5. 開始寫自己的作業前 **先開啟一個  Week1 作業的 branch** 方便之後上傳與版本管理 

   ```
   git chekout -b week1 //新建 branch 並移動至 branch
   git status //確認自己是否成功移動至 branch //
   cd homeworks/week1 //移動至作業第一週的資料夾
   open hw1.md //開啟檔案
   ```

6. 專心寫作業，內容完成後存檔。如果有 **新增的檔案** 切記要 `git add 檔名` 不然 -am 的語法是不會包含到之前沒 commit 過的檔案的！
7. `git status` 會顯示有檔案已 modified 問你要不要 commit 新版本。使用 ` git commit -am "week1"`  完成版本更新。
8. 確認交作業再看一下 [Week1 作業自我檢討](https://github.com/Lidemy/mentor-program-5th/tree/master/examples/week1)
9. 沒問題後推回雲端囉： `git push origin week1` （這時候注意是推分支回去所以是輸入 branch 的名稱 而不是 master 主幹喔）
10. 回到專案網站，若成功 push 會看到新增的 branch，選擇介面上的 **Pull requests** 對專案擁有者發動 merge to master 的請求。可以在頁面上會看到自己更動的內容等等⋯⋯。
11. 複製下 PR 後產生的連結網址，貼到繳交作業的位置，之後就是等待助教的修改與意見。
12. 若有成功被 merge 回去 master，就代表當週作業過關已完成。此時要記住同步自己個人電腦上的專案版本：（確認自己在 master 上）`git pull origin master`  把最新版本給抓下來，並  `git branch -d "week1"`  刪除掉已合併至 master的 branch week1 就完成更新啦。