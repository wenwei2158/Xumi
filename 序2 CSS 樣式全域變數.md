# 📌 序2: CSS 樣式全域變數

在 Angular 專案中，我們通常會設定 `style.scss` 作為 **全域樣式** 檔案，確保所有 CSS 規則都能影響整個應用程式。  

## **📌 設定 styles.scss**
首先，請確保在 `angular.json` 中正確引入 `styles.scss`：
```json
"styles": [
  "src/styles.scss"
]
```

>[!IMPORTANT]
>然而在專案當中並非都會把所有樣式都放在同一個檔案中，易讀性的關係會另開一個資料夾存放所有的樣式套件或是檔案，再使用@import的方式匯入到style.scss，同樣可以達成效果。
>像是以下範例:

```
src/
│── styles.scss  // 主全域樣式
│── styles/
    ├── _variables.scss   // 變數定義
    ├── _mixins.scss      // SCSS 混合樣式
    ├── _base.scss        // 基本樣式
```
如此一來可以清楚分類該專案所有套件的應用。

**以下範例**
舉最近碰到的`quill editor`編輯器為例:
-**1.新增quill-snow.scss(檔案名稱任意命名)**
