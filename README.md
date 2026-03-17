<div align="center">
  <img src="logo.png" alt="Flap Trending" width="160" />
  <h1>Flap Trending</h1>
  <p><strong>Real-Time BSC Token Analytics Dashboard</strong></p>
  <p>
    <a href="https://flaptrending.com"><img src="https://img.shields.io/badge/Live-flaptrending.com-86963088?style=for-the-badge&logo=internet-explorer&logoColor=white&color=869630" alt="Live Site"/></a>
    <a href="https://t.me/flaptrending"><img src="https://img.shields.io/badge/Telegram-Alerts-blue?style=for-the-badge&logo=telegram" alt="Telegram Alerts"/></a>
    <a href="https://t.me/flaptrendingbot"><img src="https://img.shields.io/badge/Bot-@flaptrendingbot-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram Bot"/></a>
    <img src="https://img.shields.io/badge/Chain-BSC%20Only-F0B90B?style=for-the-badge&logo=binance&logoColor=white" alt="BSC"/>
    <img src="https://img.shields.io/badge/License-Custom-red?style=for-the-badge" alt="License"/>
  </p>
</div>

---

## 🚀 Overview

**Flap Trending** is a production-ready, fully-compiled BSC token analytics dashboard built for [flap.sh](https://flap.sh) tokens. This repository distributes the **compiled frontend only** — a drop-in UI that you can self-host on any VPS or static hosting provider.

> ⚠️ **This repo contains pre-built production files only — no editable source code.**  
> The backend API server and Telegram bots are **not included** and are operated exclusively by Flap Trending.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📈 **Trending Tokens** | Real-time rankings updated every 60 seconds via `@flaptrendingbot` |
| 🆕 **New Pairs** | Newly created flap.sh bonding-curve tokens, refreshed every 10s |
| 🚀 **Top Gainers** | Biggest price movers in the last 24 hours |
| 📉 **Top Losers** | Largest drops — find opportunities before recovery |
| ⭐ **Watchlist** | Personal token list stored in your browser |
| 💱 **DEX Swap** | On-chain swap via PancakeSwap V3 + flap.sh bonding curve |
| 🤖 **@flapbuybot** | Full DEX trading bot (buy/sell/sniper/limit orders/referrals) |
| 🌐 **i18n** | English + Chinese (中文) language support |
| 🌙 **Dark UI** | Professional dark theme with olive-lime accent (`#869630`) |

---

## 🖥️ Screenshots

<div align="center">

| Trending | New Pairs | DEX Swap |
|:---:|:---:|:---:|
| Real-time rankings | Bonding curve tokens | On-chain trading |

</div>

---

## ⚙️ Self-Hosting

This is a **static SPA** (Single Page Application). Deploying is simple:

### Prerequisites

- A VPS or any static hosting (Nginx, Apache, Vercel, Netlify, Cloudflare Pages, etc.)
- HTTPS recommended

### Quick Deploy — Nginx

```bash
# 1. Clone this repo
git clone https://github.com/flaptrending/web-app-bot.git
cd web-app-bot

# 2. Copy all files to your web root
cp -r . /var/www/your-site/

# 3. Use the provided Nginx config
cp deploy/nginx.conf /etc/nginx/sites-available/your-site
# Edit the config to set your domain
nano /etc/nginx/sites-available/your-site
ln -s /etc/nginx/sites-available/your-site /etc/nginx/sites-enabled/
nginx -t && systemctl reload nginx
```

### Quick Deploy — Apache / cPanel

```bash
# 1. Clone this repo
git clone https://github.com/flaptrending/web-app-bot.git

# 2. Upload all files to your public_html
cp -r web-app-bot/. /home/your-user/public_html/

# 3. Apply the .htaccess
cp deploy/apache.htaccess /home/your-user/public_html/.htaccess
```

### Quick Deploy — Cloudflare Pages / Vercel / Netlify

1. Fork this repository
2. Connect it to Cloudflare Pages / Vercel / Netlify
3. **Build command:** *(none — files are pre-built)*
4. **Output directory:** `.` (root)

---

## 📡 Backend API

The frontend connects to the following backend endpoints. These are **operated by Flap Trending** and proxied through your web server:

| Path | Purpose |
|---|---|
| `/api/*` | Core data API |
| `/flap-gql` | flap.sh GraphQL proxy |
| `/moralis-api/*` | Token price data |
| `/bot-trending` | Live trending bot data |

> The backend API server is **not open-source** and is not included in this repository.  
> You may configure your own proxy to `https://flaptrending.com` or run a compatible server.

---

## 💱 DEX Swap & Bot — Fee Rules

> **⚠️ MANDATORY — Violation disqualifies your use of this template.**

This template includes the **DEX Swap UI** (PancakeSwap V3 + flap.sh bonding curve) and the **@flapbuybot** trading bot UI. Use of these components is permitted under the following rules:

### Fee Receiver

All swap transactions collect a **1% platform fee** sent to:

```
0x1EdbB31f17c2eEac9DbdD191990Da9BB35bF893A
```

| Rule | Requirement |
|---|---|
| 🔒 **Fee wallet** | Must remain `0x1EdbB31f17c2eEac9DbdD191990Da9BB35bF893A` |
| 💸 **Fee amount** | Must remain 1% per swap |
| 🚫 **No bypass** | You may not modify, remove, or redirect the fee |
| 📝 **Attribution** | Must credit "Powered by Flap Trending" |
| 🤖 **Bot fee** | @flapbuybot 1% fee rules apply identically |

> These rules are embedded in the compiled JavaScript and enforced at the contract level.  
> Any attempt to circumvent the fee receiver will break swap functionality.

---

## 📋 Terms of Use

By cloning, forking, or deploying this repository you agree to:

1. **Fee receiver is immutable.** The address `0x1EdbB31f17c2eEac9DbdD191990Da9BB35bF893A` must not be changed.
2. **No reverse engineering.** You may not decompile or attempt to extract source code.
3. **Attribution required.** Display "Powered by Flap Trending" visibly on your deployment.
4. **No resale.** You may not sell, sublicense, or claim ownership of this UI.
5. **BSC only.** This dashboard is designed for Binance Smart Chain only.

---

## 🤝 Official Links

| Platform | Link |
|---|---|
| 🌐 Live Dashboard | [flaptrending.com](https://flaptrending.com) |
| 📣 Alerts Channel | [t.me/flaptrending](https://t.me/flaptrending) |
| 💬 Community Group | [t.me/flaptrendingbot](https://t.me/flaptrend) |
| 🤖 Buy Bot | [@flapbuybot](https://t.me/flapbuybot) |
| 🤖 Trending Bot | [@flaptrendingbot](https://t.me/flaptrendingbot) |

---

## 🔒 Security

- Private keys and wallet encryption secrets are **never included** in this repository
- The compiled bundle contains only public-facing frontend logic
- Fee wallet is embedded in the compiled JS — tampering will break swaps

---

<div align="center">
  <img src="logo.png" alt="Flap Trending" width="64" />
  <br/>
  <strong>Built with ❤️ by the Flap Trending team</strong>
  <br/>
  <sub>© 2025 Flap Trending — All rights reserved</sub>
</div>
