# 📌 補充: Git 版本控制、專案打包、更新開發站

## 📌**Git版本控制**
在IDE環境中左側邊欄有一個source control按鈕，顯示git flow節點圖，當然可以直接操作所有的git指令。然而有一個工具可以更直覺化且便利操作，`sourcetree`: 是一款提供 GUI 界面來管理版本控制內容的軟體，讓你可以直接在這款軟體內看到每一個 Branch 的線圖，從修改 並 Commit 到 Branch 的動作，或是在節點上加上 Tag 來方便管理。

- 通常以main當作主要分支，或是以develop為主要開發分支，依照每個起始專案規定不同。
- git 的方法有許多，常用`commit`、`push`、`branch`、`merge`、`checkout`，詳細使用方法可以參考

>[!IMPORTANT]
>如果分支以push到遠端，但想要反悔並不保留紀錄可以使用`git reset`，**切記，請小心使用**，以下為使用步驟:
>- 1.git checkout到要異動的分支
>- 2.git reset --hard <reflog-hash>
>- 3.git push --force

## 📌**專案打包**
>[!NOTE]
>這裡提到如何clone gitlab專案到地端:
>- 1.首先到gitlab，點選欲複製的專案，點選右上角程式碼以HTTPS複製，
>- 2.開啟終端機或是IDE環境，在指定資料夾下執行 `git clone https://pisb-gitlab.kh.elearn.com.tw/angular-developers/motcmpb.git`
>- 3.由於主機有更換過，所以要確定.gitmodules檔案中的遠端資料庫位置是否正確。詳細可參考(XUMI為例)
>- ![{F2E0FED8-1C3E-46B4-8D11-A4981E0F9DFA}](https://github.com/user-attachments/assets/1f8a83aa-1248-4169-93eb-c9671443d7df)

打包專案步驟很簡單，在終端機執行`npm run build:web`即可。**注意，當失敗時可以詳閱錯誤訊息，有可能發生commit，push都正常的況下，但打包時異常，可以利用錯誤訊息查找並記錄下，預防再次發生**

## 📌**更新開發站**
當打包完成後，打開資料夾中`dist`資料夾，`web`資料夾表示網頁版已包裝程式代碼，我們會利用這個資料夾更新網芳站台裡的檔案
- 打開網芳指定資料夾，進到`mocs_angular`，將`web`資料夾內的檔案清空，再將打包後的資料搬移至`web`即可

>[!IMPORTANT]
>- 1.當要更新開發站時，打包專案時必須要確定檔案室否已推送到遠端，否則打包後的檔案有機率會無法使用。
>- 2.更新`web`時，為了預防新的打包檔案出錯，可以將原本的web壓縮，以便在更新後檔案異常造成站台錯誤時，可以使用壓縮檔復原回上一版。

---
參考文件
- 📌[git文件](https://git-scm.com/book/zh-tw/v2/%E9%96%8B%E5%A7%8B-%E9%97%9C%E6%96%BC%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6)
- 📌[學習git分支](https://learngitbranching.js.org/?locale=zh_TW)



