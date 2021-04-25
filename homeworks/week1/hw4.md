## Week1-hw4 跟你朋友介紹 Git

#### 介紹Git

聰明喔！菜哥知道要用 Git 來處理不同笑話的版本。我也是最近才知道XD
Git 的主要目的就是電腦的**版本控制**，檔案（或專案）製作過程中，隨時間與需求更迭會產生出許多不同版本；希望藉系統將每個檔案版本都保存（並記錄清楚）起來。運作架構可以 **用資料夾的方式來理解**，資料夾區分整理各版本（使用**亂數碼**作為名稱，以防各種邏輯命名衝突，例如：同事之間大家檔名都一樣），並在外部檔案註記順序與最新版本以辨別亂數檔名；不需要版本控制的檔案則不需要加入資料夾（例如：電腦的設定檔或隱私密碼等跟版本內容無關的）。除了各線性的版本控制外，還能創建 **branch 分支**的系統，提供多線同步作業再合併版本，達到最有效的版本控制。

___

* 練習基本 git 指令

`git init` git initialized 初始化，對專案建立版本控制資料夾 (.git）
`git status` 確認檔案的版本控制狀態 
`git add`  決定是否加入版本控制，檔案會被分為兩種區塊 

>（ changes to be committed ）unstage 加入版本控制 //（untracked files ）不加入

`git rm --cached`  檔案移出版本控制
`git commit` 正式新建版本 （ 新建完成後會跳入 git 的 vim 文字編輯器，可進去輸入版本 message ）
或使用 `git commit -m "版本名稱命名"` （ m message的意思 ）

> 這邊注意：務必先 add 再 commit，先把檔案分類加不加入版本控制，才能建立新版本
>
> 合併技：`git commit -am "_name_"`（ a 就是 all 的意思，已 commit 過的全部檔案，但不包含新建檔案！新檔還是必須用 add 加入版本控制範圍後才能commit ）
>
> 可使用 --amend 來修改最後一次的 commit 紀錄，例：`git commit --amend -m "3rd edition"`，他會以新的 commit 取代舊的，所以亂數名也不同，若要修改的 commit 已被 push 到遠端千萬避免私自修改

`git log` 版本歷史紀錄，會紀錄每個版本獨特的號碼（似亂碼）、作者、時間等 （參數 --oneline 可顯示簡短的log樣式）

`git checkout` 回到過去某版本 `git checkout 版本亂碼號碼`（ 若使用參數 master 則會再度回到最新版本 ）
`touch .gitignore` 忽略檔案，任何冠入的檔案都會被 git 忽略 （他是一個檔案喔，要用 touch 新建）

> vim .gitignore 進入 vim 將欲忽略的檔名key入

`git diff` 查看改了什麼 

* branch相關指令

`git branch -v`  查看有哪些 branch 分支

`git branch  ` 建立分支 （合併技：`git checkout -b branchname`  建立新 branch 再移動到 branch ）

`git branch -d ` 刪除分支

`git checkout branchname` 移動到分支的檔案 （ checkout 指令可以在版本或分支之間移動 ）

`git merge` 把分支合併進來（遇到衝突的話，就手動解決）

---

#### 菜哥笑話版本控制

1. 先安裝好 git `git --version` 確認目前電腦使用的 git 版本
2. 移動到 joke 資料夾位置 `cd ~/..../joke ` 
3. 將資料夾加入版本控制 `git init`
4. `git status` 確認目前 git 狀態
5. `touch .gitignore` （把裡面跟笑話無關的檔名寫入vim吧，這樣就不會加入版本控制了）
6. 繼續修改笑話檔案（此時菜哥有新增了笑話a檔）
7. `git add a檔`（a檔是新增檔，一定要先加入版本控制)
8. `git commit -am "1st_edition"`（加入版本控制）`git log` （查看目前版本控制紀錄會顯示1st_ediotion）
9. 成功囉，這時候請菜哥創建一個 Github 的帳號，來用雲端同步版本。
10. 在帳號裡開啟一個 joke 的 repository ，複製專案生成的網址到 terminal 進行連線。
11. 使用 `git push origin master` 把目前的笑話版本上傳！（要抓取雲端版本下來，指令改 pull ）