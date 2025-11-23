# Clipalette

一鍵複製，隨處貼上

[English](README.md) | [正體中文](docs/README.zh_TW.md)

![Screenshot](./screenshots/screenshot.v2.png)

Clipalette 是一款簡潔、輕量、易於客製的快速複製面板工具，  
讓常用字串、符號與片語變成可點擊的按鈕，提高輸入效率。

- 🪶 高度客製化：  
  可輕鬆調整、擴充、或建立自己的字串庫。
- 📄 單一檔案即可運作：  
  純 HTML / CSS / JavaScript，不依賴任何外部框架，也無需編譯。
- ✈️ 完全離線執行。
- 📱 支援行動裝置。
- 🎨 三種外觀：  
  🌐 自動、🌞 明亮、和 🌚 闇黑模式。
- 📑 多分頁面板：  
  以分頁區分不同集合，清楚、直覺、可擴充。
- 🆕：兩種模式：  
  ⚡ 自動和 👋 手動模式。
- 🧠 自動記憶設定：
  包括色彩主題、模式、和上次的分頁。

## 如何使用

1. 點選分頁按鈕切換分頁；
1. 選擇模式；
    - ⚡ 自動模式：點擊按鈕即複製其內容；
    - 👋 手動模式：點擊按鈕會串接其內容後再複製。
1. 點擊按鈕選擇要複製的內容。
1. 點擊 🧹 按鈕可以清空當前輸出。
1. 點擊 📋 按鈕可以再次複製。

## 定製

編輯 Clipalette 的原始碼（以 txt 純文字檔方式開啟）；
在檔案的開頭不遠處，仿照格式編輯變數 `buttonMap`；

```javascript
var buttonMap = {
    "Some Tab": [
        ["Foo", "Bar"],
        ["Bla bla bla..."]
    ], "Another Tab": [
        ["A Lonely Button"]
    ]  // , ...
}
```

- 每個物件（object）代表一個分頁，屬性（key）是「分頁標題」；
- 每個分頁中可以有多個陣列（array），每個陣列是「一列（row）按鈕」；
- 每列可以有多個字串，每個字串代表按鈕上顯示的文字並會被複製；

儲存後重新整理（`F5`）即可看到結果。

---

Reference:

- Color theme comes from [chriskempson/tomorrow-theme](https://github.com/chriskempson/tomorrow-theme) (MIT)
- A small part of CSS is borrowed from the [teacat/tocas](https://github.com/teacat/tocas) (MIT)
