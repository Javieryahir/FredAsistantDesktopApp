# 🖥️ Electron + React + Vite App

This project is a **desktop app** built with **Electron**, **React**, and **Vite**.  
It includes **hot reload** during development and a production-ready build.

---

## 📁 Project Structure

/my-project
├─ package.json
├─ electron.js <- Electron main process
├─ vite.config.js <- Vite configuration
├─ /src
│ ├─ main.jsx <- React entry point
│ └─ App.jsx
└─ index.html <- Vite HTML template

---

## ⚡ Requirements

- Node.js >= 18
- npm >= 9
- Operating system: Windows, macOS, or Linux

---

## 💻 Installation

git clone https://github.com/username/my-project.git
cd my-project
npm install
🚀 Development with Hot Reload
bash
Copy code
npm run dev
Runs Vite for React and Electron at the same time.

Hot reload works automatically for React components.

To enable hot reload for the main process (electron.js), install:

bash
Copy code
npm install electron-reload --save-dev
Then add at the top of electron.js:

javascript
Copy code
if (require('electron-is-dev')) {
require('electron-reload')(**dirname, {
electron: require(`${**dirname}/node_modules/electron`)
});
}
🏗️ Production Build
Build the React app:

bash
Copy code
npm run build
Package the app with Electron Builder:
npm run dist
This will create an executable for your operating system.

React files are included in the dist/ folder.

⚙️ Useful Scripts
Command Description
npm run dev:vite Run only Vite (React) with hot reload
npm run dev:electron Start Electron pointing to the Vite server
npm run dev Run Vite + Electron together for full development
npm run build Generate React build (dist/)
npm run start Start Electron loading the production build
npm run dist Package the app with electron-builder

```

```
