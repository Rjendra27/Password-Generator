# 🔐 Random Password Generator

A simple, clean web app that generates strong random passwords in your browser. No dependencies, no build tools — just HTML, CSS, and JavaScript.

![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-yellow)
![HTML5](https://img.shields.io/badge/HTML5-orange)
![CSS3](https://img.shields.io/badge/CSS3-blue)

## ✨ Features

- Generates two random 15-character passwords at once
- Uses uppercase letters, lowercase letters, numbers, and special characters
- One-click generation
- Click-to-select password text for easy copying
- Minimal, dark-themed UI
- No external libraries or frameworks — pure vanilla JS

## 🚀 Demo

🔗 **Live site:** [a-random-passwordgenerator.netlify.app](https://a-random-passwordgenerator.netlify.app/)

Or open `index.html` in any modern browser and click **Generate Passwords**.

## 📂 Project Structure

```
.
├── index.html   # Markup and structure
├── index.css    # Styling (dark theme, card layout)
└── index.js     # Password generation logic
```

## 🛠️ Getting Started

### Prerequisites

Just a web browser — no installation required.

### Run locally

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Open `index.html` directly in your browser, or serve it locally:
   ```bash
   npx serve .
   ```

## ⚙️ How It Works

`index.js` builds each password by randomly picking characters from a predefined character set (letters, numbers, and symbols) for a fixed length (currently 15 characters):

```js
function getRandomPassword() {
    let password = ""
    for (let i = 0; i < passwordLength; i++) {
        let randomIndex = Math.floor(Math.random() * characters.length)
        password += characters[randomIndex]
    }
    return password
}
```

Clicking **Generate Passwords** fills in two password slots on the page with freshly generated values.

## 🎨 Customization

- **Password length** — change the `passwordLength` variable in `index.js`
- **Character set** — edit the `characters` array in `index.js` to add/remove symbols
- **Theme/colors** — adjust CSS variables and colors in `index.css`

## 🗺️ Roadmap / Ideas

- [ ] Add a length slider/input for user-adjustable password length
- [ ] Add checkboxes to toggle character types (uppercase, numbers, symbols)
- [ ] Add a "Copy to clipboard" button
- [ ] Add a password strength indicator

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
