# 🧮 Standalone PDF Calculator

A fully functional calculator embedded *inside* a standalone PDF — built with pure PDF form fields and JavaScript.  
No HTML. No web tech. Just cursed PDF sorcery. 💀📄

## ⚡ Features
- Basic operations: `+`, `-`, `*`, `/`
- 100% standalone — no internet or external scripts
- Runs entirely within the PDF
- Works in **Adobe Acrobat Reader**
- (😱 Also works in Chrome/Edge PDF viewers — unexpectedly)

## 📦 How It Works
- PDF created using **Adobe Acrobat Pro**
- Uses PDF form fields (`num1`, `num2`, `operation`, `result`)
- A button runs this JavaScript:

```js
var a = parseFloat(this.getField("num1").value);
var b = parseFloat(this.getField("num2").value);
var op = this.getField("operation").value;
var res;

switch(op) {
  case "+": res = a + b; break;
  case "-": res = a - b; break;
  case "*": res = a * b; break;
  case "/": res = b !== 0 ? a / b : "∞"; break;
  default: res = "Error";
}

this.getField("result").value = res;
```

## ⚠️ Notes
- Use **Adobe Acrobat Reader** for full functionality.
- Doesn't work on macOS Preview or some lightweight PDF viewers.
- Browser compatibility is a fluke. Use with awe 😈

## 📁 Files
- `calculator.pdf` – the cursed PDF
- `README.md` – this doc

---

Built for no reason. Runs against logic. Works anyway.
