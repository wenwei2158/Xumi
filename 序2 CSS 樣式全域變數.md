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
>然而在專案當中並非都會把所有樣式都放在同一個檔案中，易讀性的關係會另開一個資料夾存放所有的樣式套件或是檔案，再使用`@import`的方式匯入到`style.scss`，同樣可以達成效果。
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

## 📌**以下範例**
舉最近碰到的`quill editor`編輯器為例:
- **1.新增quill-snow.scss(檔案名稱任意命名)**，若要引用套件則需要依照版本規則在專案內執行npm install(套件名稱/版本)並且執行`npm install`更新node_modules內套件，才能夠引入使用。
>[!NOTE]
> quill使用了三個套件，`@type/quill: ^1.3.`、`@ngx-quill: ^19.0.1`、`@quill: 1.3.7`。
- **引用至style.scss**
- **在quill-snow.scss中設定該有的樣式**
- **根據套件使用位置決定引入，quill必須在`app.module.ts`中引入才能使用，依循編輯器預設以及客製化也有所不同，詳細請參考XUMI develop**
