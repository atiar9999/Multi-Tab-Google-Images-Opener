```markdown
# 🚀 Multi‑Tab Google Images Opener

![Preview](https://via.placeholder.com/800x400.png?text=Multi-Tab+Google+Images+Opener+Demo)  
*A sleek, client‑side tool to open multiple Google Images searches from a list of words – with CAPTCHA‑avoiding delays.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## ✨ Features

- **Bulk tab opening** – Type one word per line, click a button, and get a Google Images search tab for each word.
- **CAPTCHA protection** – Built‑in delay option (0.3s to 2s) spaces out tab openings, reducing the chance of triggering Google’s CAPTCHA.
- **Smart pop‑up handling** – First tab opens immediately (best chance to bypass pop‑up blockers), remaining tabs open with your chosen delay.
- **Modern UI** – Clean, minimal interface with glassmorphism, smooth animations, and responsive design.
- **Word counter** – Real‑time count of non‑empty lines.
- **Fully client‑side** – No server, no tracking, no dependencies. Works offline.

---

## 📦 Installation & Usage

1. **Download** or clone this repository:
   ```bash
   git clone https://github.com/yourusername/multi-tab-image-opener.git
   ```
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
3. **Allow pop‑ups** for this page when prompted (or click the pop‑up icon in your address bar).
4. Enter your words – one per line – in the text area.
5. Toggle the **“Add delay between tabs”** option and select a delay if you want to avoid CAPTCHA.
6. Click **“Open all in Google Images”**.
7. Watch the tabs open!

> ⚠️ **Important**  
> Pop‑up blockers may interfere with delayed tabs. If some tabs don’t open, try a shorter delay or disable the delay entirely.  
> Opening 30+ tabs at once may slow down your browser.

---

## ⚙️ How It Works

The tool reads the textarea, splits it by newlines, and trims each line.  
For every non‑empty word, it constructs a Google Images URL:
```
https://www.google.com/search?tbm=isch&q=ENCODED_WORD
```
If **delay is off**, all tabs open immediately (synchronously) in the click event.  
If **delay is on**, the first tab opens instantly, and the rest open after `i * delayMs` using `setTimeout`. This mimics human behaviour and reduces automated request flags.

---

## 🛠️ Customization

All styles are contained in a separate `styles.css` file (the one provided in the answer). You can easily:

- Change colours, fonts, or spacing via CSS variables (`:root`).
- Adjust the delay options in the `<select>` menu (edit the `value` attributes).
- Modify the base Google search URL (e.g., change `tbm=isch` to another search type).

Example: to change the delay values, edit the `delaySelect` options in the HTML:
```html
<select id="delaySelect">
  <option value="300">0.3 sec</option>
  <option value="500" selected>0.5 sec</option>
  ...
</select>
```

---

## 🧰 Technologies Used

- **HTML5** – semantic structure
- **CSS3** – custom properties, flexbox, glassmorphism, animations, responsive design
- **Vanilla JavaScript (ES6)** – no frameworks, no dependencies

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  


1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 🙏 Acknowledgements

- Google Images for being the search target.
- The amazing open‑source community for design inspiration.

---

Made with ❤️ by Atiar
```
