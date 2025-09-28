# 🖥️ Electron + React + Vite App

This project is a **desktop application** built using **Electron**, **React**, and **Vite**.  
It supports **hot reload** during development and is ready for production builds.

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

yaml
Copy code

---

## ⚡ Requirements

- Node.js >= 18
- npm >= 9
- Operating system: Windows, macOS, or Linux

---

## 💻 Installation

1. Clone the repository:

```bash
git clone https://github.com/username/my-project.git
cd my-project
Install dependencies:

bash
Copy code
npm install
🚀 Development with Hot Reload
Run both React (Vite) and Electron together:

bash
Copy code
npm run dev
Hot reload works automatically for React components.

To enable hot reload for the Electron main process (electron.js):

bash
Copy code
npm install electron-reload --save-dev
Then, add the following at the top of electron.js:

javascript
Copy code
import isDev from 'electron-is-dev';
import path from 'path';

if (isDev) {
  import('electron-reload')(`${__dirname}`, {
    electron: path.join(__dirname, 'node_modules', '.bin', 'electron')
  });
}
🏗️ Production Build
Build the React app:

bash
Copy code
npm run build
Package the app with Electron Builder:

bash
Copy code
npm run dist
This creates an executable for your operating system.

The built React files are included in the dist/ folder.

⚙️ Useful Scripts
Command	Description
npm run dev:vite	Run only Vite (React) with hot reload
npm run dev:electron	Start Electron pointing to the Vite server
npm run dev	Run Vite + Electron together (full dev)
npm run build	Generate React build (dist/)
npm run start	Start Electron loading the production build
npm run dist	Package the app with electron-builder
```
