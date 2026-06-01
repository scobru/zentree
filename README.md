# 🌳 ZenTree — Decentralized P2P Personal Portal

ZenTree is a lightweight, responsive, and completely **decentralized personal portal template** (Linktree clone) that runs entirely serverless. It enables developers to host their own landing page along with a suite of end-to-end encrypted micro-apps (Notes, Bookmarks, Keep Vault) on any static web host for free.

Powered by **ZEN**—a zero-config decentralized peer-to-peer graph database.

## 🚀 Live Demo Structure

The project comes pre-configured with three decentralized utilities:
1. 📝 **Notes App**: Offline-first, decentralized markdown workspace for publishing public notes or saving draft logs.
2. 🔖 **Bookmarks App**: Secure, decentralized bookmark manager categorized dynamically.
3. 🔒 **Keep Vault**: An **End-to-End Encrypted (E2EE)** private data store. All records are cryptographically encrypted in-browser before syncing to the P2P network.

---

## 🛠️ Features

- 🌐 **100% Serverless**: No backend, no SQL, no configuration. Served strictly as static HTML, CSS, and JS.
- ⚡ **Real-Time P2P Sync**: Automatically updates and syncs modifications across peers in real-time.
- 🔐 **Cryptographic Auth**: Derives high-entropy cryptographic keypairs locally in-browser using Master Credentials (passwordless username + passphrase).
- 🎨 **Premium Aesthetic**: Curated light/dark theme modes, Outfit & IBM Plex Mono typography, responsive grids, and clean micro-animations.
- 📦 **Zero Dependencies**: Zero build tools, zero node packages. Loads everything instantly via CDN (Unpkg & Tabler Icons).

---

## 💻 Setup & Deployment

Setting up your own ZenTree is incredibly simple and takes under 5 minutes:

### 1. Fork & Clone
Clone this repository to your local system:
```bash
git clone https://github.com/your-username/zentree.git
```

### 2. Configure Cryptographic Public Keys
For the portal to load your specific links without authentication, you need to configure your public view key:
1. Open **`key-generator.html`** in your browser.
2. Input your desired secure **Username** and **Password** (your Master Credentials) and click **Derive Public Key**.
3. Copy the derived public view key.
4. Open `index.html`, `apps/bookmarks.html`, and `apps/notes.html`.
5. Locate `PUBLIC_VIEW_KEY` and paste your key inside the empty quotes:
   ```javascript
   const PUBLIC_VIEW_KEY = 'YOUR_DERIVED_KEY_HERE';
   ```

### 3. Seed Default Templates
After authenticating inside **Manage Portal** for the first time:
- Click **Seed Defaults** to instantly write a set of beautiful initial templates to your database node!
- You can now add, edit, or delete any links directly in real-time. Simply hover over any link when logged in to see the red deletion action button.

### 4. Deploy Anywhere
Simply push your repository to GitHub and enable **GitHub Pages** (Settings -> Pages) or drop the files onto any static hosting platform.

---

## 🌐 Recommended P2P Relays

ZenTree is pre-configured to sync data across these recommended decentralized peer-to-peer relays:
- `wss://delay.scobrudot.dev/zen`
- `wss://zen.akao.io:8420/zen`
- `wss://zen0.akao.io:8420/zen`
- `wss://zen1.akao.io:8420/zen`

### 🚀 Spin Up Your Own Relay
To ensure maximum availability, data longevity, and self-sovereignty, you can run your own dedicated peer. Check out the [ZEN Relay Deployment Guide](https://github.com/akaoio/zen#deploy-a-relay-peer) to deploy your own relay with one single command.

---

## 🎨 Tech Stack

- **HTML5 & Vanilla CSS**: Premium modern style patterns, responsive flexbox/grid layout, and dynamic HSL color variables.
- **P2P Database**: [ZEN P2P Graph Engine](https://github.com/akaoio/zen) loaded dynamically via CDN.
- **Icons**: [Tabler Icons Webfont](https://tabler.io/icons).
- **Fonts**: Outfit & IBM Plex Mono via Google Fonts CDN.

---

## 📄 License
This project is open-source and free to use under the MIT License. Customize it, build on it, make it yours!
