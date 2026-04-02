<div align="center">
  <img src="logo.png" alt="4Trend" width="160" />
  <h1>4Trend</h1>
  <p><strong>Real-Time BSC Token Analytics Dashboard</strong></p>
  <p>
    <a href="https://4trend.vercel.app"><img src="https://img.shields.io/badge/Live-4trend.vercel.app-86963088?style=for-the-badge&logo=internet-explorer&logoColor=white&color=869630" alt="Live Site"/></a>
    <a href="https://t.me/flaptrending"><img src="https://img.shields.io/badge/Telegram-Alerts-blue?style=for-the-badge&logo=telegram" alt="Telegram Alerts"/></a>
    <a href="https://t.me/flaptrendingbot"><img src="https://img.shields.io/badge/Bot-@flaptrendingbot-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram Bot"/></a>
    <img src="https://img.shields.io/badge/Chain-BSC%20Only-F0B90B?style=for-the-badge&logo=binance&logoColor=white" alt="BSC"/>
    <img src="https://img.shields.io/badge/License-Custom-red?style=for-the-badge" alt="License"/>
  </p>
</div>

---

## 🚀 Overview

**4Trend** is a production-ready, fully-compiled BSC token analytics dashboard built for [four.meme](https://four.meme) tokens. This repository distributes the **compiled frontend only** — a drop-in UI that you can self-host on any VPS or static hosting provider.

> ⚠️ **This repo contains pre-built production files only — no editable source code.**  
> The backend API server and Telegram bots are **not included** and are operated exclusively by 4Trend.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📈 **Trending Tokens** | Real-time rankings updated every 60 seconds via `@flaptrendingbot` |
| 🆕 **New Pairs** | Newly created four.meme bonding-curve tokens, refreshed every 10s |
| 🚀 **Top Gainers** | Biggest price movers in the last 24 hours |
| 📉 **Top Losers** | Largest drops — find opportunities before recovery |
| ⭐ **Watchlist** | Personal token list stored in your browser |
| 💱 **DEX Swap** | On-chain swap via PancakeSwap V3 + four.meme bonding curve |
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
1. Connect it to Cloudflare Pages / Vercel / Netlify
2. **Build command:** *(none — files are pre-built)*
3. **Output directory:** `.` (root)

---

## 📡 Backend API

The frontend connects to the following backend endpoints. These are **operated by 4Trend** and proxied through your web server:

| Path | Purpose |
|---|---|
| `/api/*` | Core data API |
| `/flap-gql` | four.meme GraphQL proxy |
| `/moralis-api/*` | Token price data |
| `/bot-trending` | Live trending bot data |

> The backend API server is **not open-source** and is not included in this repository.  
> You may configure your own proxy to `https://4trend.vercel.app` or run a compatible server.

---

## 💱 DEX Swap & Bot — Fee Rules

> **⚠️ MANDATORY — Violation disqualifies your use of this template.**

This template includes the **DEX Swap UI** (PancakeSwap V3 + four.meme bonding curve) and the **@flapbuybot** trading bot UI. Use of these components is permitted under the following rules:

---

## 📋 Terms of Use

By cloning, forking, or deploying this repository you agree to:

2. **No reverse engineering.** You may not decompile or attempt to extract source code.
3. **Attribution required.** Display "Powered by 4Trend" visibly on your deployment.
4. **No resale.** You may not sell, sublicense, or claim ownership of this UI.
4. **BSC only.** This dashboard is designed for Binance Smart Chain only.

---

## 🤝 Official Links

| Platform | Link |
|---|---|
| 🌐 Live Dashboard | [4trend.vercel.app](https://4trend.vercel.app) |
| 📣 Alerts Channel | [t.me/flaptrending](https://t.me/flaptrending) |
| 💬 Community Group | [t.me/flaptrendingbot](https://t.me/flaptrend) |
| 🤖 Buy Bot | [@flapbuybot](https://t.me/flapbuybot) |
| 🤖 Trending Bot | [@flaptrendingbot](https://t.me/flaptrendingbot) |

---

## 🔒 Security

- Private keys and wallet encryption secrets are **never included** in this repository
- The compiled bundle contains only public-facing frontend logic

---

<div align="center">
  <img src="logo.png" alt="4Trend" width="64" />
  <br/>
  <strong>Built with ❤️ by the 4Trend team</strong>
  <br/>
  <sub>© 2025 4Trend — All rights reserved</sub>
</div>
