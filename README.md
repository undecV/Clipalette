# Clipalette

Copy Once, Paste Everywhere

[English](./README.md) | [繁體中文](./docs/README.zh_TW.md)

![Screenshot](./docs/screenshots/screenshot.v2.png)

Clipalette is a simple, lightweight, and highly customizable copy panel  
that turns frequently used strings, symbols, and phrases into clickable buttons—  
helping you work faster and type less.

- 🪶 **Highly customizable:**  
  Easily edit, extend, or build your own string collections.
- 📄 **Single-file application:**  
  Pure HTML / CSS / JavaScript. No dependencies, no build process required.
- ✈️ **Works completely offline.**
- 📱 **Mobile-friendly layout.**
- 🎨 **Three appearance modes:**  
  🌐 Auto, 🌞 Light, and 🌚 Dark.
- 📑 **Multiple tabs:**  
  Organize strings into separate groups for clarity and scalability.
- 🆕 **Two modes:**  
  ⚡ Auto mode and 👋 Manual mode.
- 🧠 **Persistent settings:**  
  Remembers the selected theme, mode, and last opened tab.

---

## How to Use

1. Click a tab to switch between groups.
2. Choose a mode:
    - ⚡ **Auto Mode:** Clicking a button copies its content immediately.
    - 👋 **Manual Mode:** Clicking a button appends its content to the output field;  
      copy when you're ready.
3. Click a button to select the content you want to copy.
4. Use the 🧹 button to clear the output field.
5. Use the 📋 button to copy the output again.

---

## Customization

Open the Clipalette source file (a plain text `.html` file).  
Near the top of the file, locate the variable `buttonMap` and edit it following the format:

```javascript
var buttonMap = {
    "Some Tab": [
        ["Foo", "Bar"],
        ["Bla bla bla..."]
    ],
    "Another Tab": [
        ["A Lonely Button"]
    ]  // , ...
}
```

- Each **object key** represents a **tab title**.
- Each key contains one or more **arrays**, and **each array is a row of buttons**.
- Each **string** becomes a button, and clicking the button copies that string.

Save the file and refresh the page (`F5`) to see the changes.

---

Reference:

- Color theme comes from [chriskempson/tomorrow-theme](https://github.com/chriskempson/tomorrow-theme) (MIT)
- A small part of CSS is borrowed from the [teacat/tocas](https://github.com/teacat/tocas) (MIT)
