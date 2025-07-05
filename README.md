# Crypto Runner 🏃‍♂️💨

Crypto Runner is an endless-runner web game spiced up with optional blockchain extras. Dodge obstacles, grab coins, upgrade your booster/shield… and (if you feel like it) connect your MetaMask wallet to save scores on-chain and tip the devs.

---

## 1. Demo

Play the deployed version 👉 **https://crypto-runner.vercel.app**

*(If you are on mobile, rotate to landscape for the best experience.)*

---

## 2. Project structure

```text
Crypto-Runner/
├── game/               # Source code (HTML, JS, assets)
│   ├── index.html
│   ├── style.css
│   ├── vite.config.js  # Vite bundler config
│   ├── package.json    # Scripts & deps (ethers v6)
│   ├── scripts/        # Game logic, walletConnect, service-worker register
│   └── assets/         # Sprites, audio, GUI
├── README.md           # ← you are here
└── .git
```

---

## 3. Prerequisites

* **Node 18 LTS** or newer (includes `npm`)
* A modern browser (Chrome, Edge, Firefox, or Safari)
* _Optional:_ MetaMask or another EVM wallet for blockchain features

---

## 4. Getting started locally

```bash
# clone if you haven't already
# git clone https://github.com/<you>/Crypto-Runner.git

cd Crypto-Runner/game
npm install            # installs Vite + ethers

# start local dev server (auto-reload + HMR)
npm run dev
# → http://localhost:5173
```

### Production build

```bash
npm run build          # outputs static files to dist/
# Preview the built bundle
npm run preview        # http://localhost:4173
```

---

## 5. Controls

* **Desktop** – W/A/S/D or ← ↑ ↓ → (jump / slide / move)
* **Mobile**  – on-screen buttons (appear automatically on touch devices)
* **P** – Pause

---

## 6. Blockchain integration

* Uses **ethers v6** (bundled) and a lightweight script at `scripts/walletConnect.js`.
* Click **"connect wallet"** on the main menu to:
  1. Request wallet connection
  2. Prompt switch to **Filecoin Calibration Testnet** (auto-added if absent)
  3. Show truncated address + tFIL balance in the button

Feel free to fork & extend: submit scores to a contract, mint NFTs for achievements, etc.

---

## 7. Progressive Web App (PWA)

Crypto Runner ships with a simple **service-worker** (cache-first) so it can be installed and played offline.

* `fav/site.webmanifest` – icons & metadata
* `sw.js` – asset caching

---

## 8. Development roadmap

| Task | Status |
|------|--------|
| Folder cleanup (`Cgg_game → game`) | ✅ done |
| Vite dev & build scripts | ✅ done |
| ESLint + Prettier baseline | ✅ done (warnings remain) |
| WalletConnect upgrade (ethers v6) | ✅ done |
| PWA (manifest + SW) | ✅ done |
| Asset optimisation (spritesheet compression) | _todo_ |
| Unit tests (Jest) | _todo_ |
| GitHub Actions CI (lint → test → build) | _todo_ |

Contributions welcome! Open a PR or issue if you have ideas.

---

## 9. License

MIT © 2025 Your Name
