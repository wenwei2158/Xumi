# 📌 補充: Git 版本控制、專案打包、更新開發站

## 📌**Git版本控制**
在IDE環境中左側邊欄有一個source control按鈕，顯示git flow節點圖，當然可以直接操作所有的git指令。然而有一個工具可以更直覺化且便利操作，`sourcetree`: 是一款提供 GUI 界面來管理版本控制內容的軟體，讓你可以直接在這款軟體內看到每一個 Branch 的線圖，從修改 並 Commit 到 Branch 的動作，或是在節點上加上 Tag 來方便管理。

>[!IMPORTANT]
>如果分支以push到遠端，但想要反悔並不保留紀錄可以使用`git reset`，**切記，請小心使用**，以下為使用步驟:
>- 1.git checkout到要異動的分支
>- 2.git reset --hard <reflog-hash>
>- 3.git push --force

## 📌**專案打包**
>[!NOTE]
>這裡提到如何clone gitlab專案道地端:
>1.首先到gitlab，點選欲複製的專案，點選右上角程式碼以HTTPS複製，
>2.開啟終端機或是IDE環境，在指定資料夾下執行 `git clone https://pisb-gitlab.kh.elearn.com.tw/angular-developers/motcmpb.git`
>3.由於主機有更換過，所以要確定.gitmodules檔案中的遠端資料庫位置是否正確。詳細可參考(XUMI為例)
>![{F2E0FED8-1C3E-46B4-8D11-A4981E0F9DFA}](https://github.com/user-attachments/assets/1f8a83aa-1248-4169-93eb-c9671443d7df)

打包專案步驟很簡單，在終端機執行`npm run build:web`

---
參考文件
- 📌[sourcetree 安裝流程](https://ithelp.ithome.com.tw/articles/10206852)




