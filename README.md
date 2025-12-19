# Limkid‑X — Modern WhatsApp Bot 

<p align="center">
  <img src="https://files.catbox.moe/o2zvp8.jpg" alt="Limkid-X" width="700"/>
</p>

<p align="center">
  <strong>Limkid‑X</strong> — a powerful, multi‑feature WhatsApp automation bot for groups, media tools, moderation and more. Deploy in minutes and run like an app.
</p>

<!-- Typing animation: types "Limkid-X Whatsapp bot", then deletes and types "by jay von" -->
<p align="center">
  <img alt="Typing animation" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=2500&color=ff00ab&center=true&vCenter=true&multiline=true&width=700&height=48&lines=Limkid-X+Whatsapp+bot;by+jay+von" />
</p>

<p align="center">
  <a href="https://github.com/jayvon33/limkid-X/fork"><img alt="Fork" src="https://img.shields.io/badge/FORK-LIMKID--X-blue?style=for-the-badge"/></a>
  <a href="https://pairlimkid-f0adcc9718da.herokuapp.com/pair"><img alt="Get Pair Code" src="https://img.shields.io/badge/Get%20Pair%20Code-%23ffcc00?style=for-the-badge&logo=webhook"/></a>
  <a href="https://pairlimkid-f0adcc9718da.herokuapp.com/qr"><img alt="Get QR Pair" src="https://img.shields.io/badge/QR%20Pair-%2300b7ff?style=for-the-badge&logo=qr-code"/></a>
  <a href="https://dashboard.heroku.com/new?template=https://github.com/jayvon33/limkid-X"><img alt="Deploy to Heroku" src="https://www.herokucdn.com/deploy/button.svg"/></a>
  <a href="https://render.com/deploy?repo=https://github.com/jayvon33/Limkid-X.git"><img alt="Deploy to Render" src="https://render.com/images/deploy-to-render-button.svg"/></a>
</p>

---

## Quick Preview

<p align="center">
  <img src="https://media.tenor.com/rePDfDWO3XoAAAAd/hacking.gif" alt="Demo" width="480"/>
</p>

---

## Key Features

- App-like, easy-to-follow setup and deployment
- Pairing (SESSION_ID) or QR pairing UI for quick bot login
- Group management: moderation, welcome/leave messages, anti-spam
- Media tools: image/audio processing, sticker creation, converters
- Automation: scheduled tasks, auto‑reply, command handlers
- Plugin-friendly: extend commands and modules easily

---

## Pairing & Sessions

You can pair your WhatsApp session using either the Pairing website (session ID) or the QR Pair:

- Pairing website (session ID): https://pairlimkid-f0adcc9718da.herokuapp.com/pair  
  Click the link, copy the displayed Session ID and add it to your environment variables as `SESSION_ID`.

- QR Pair (scan with your phone): https://pairlimkid-f0adcc9718da.herokuapp.com/qr

Important: Keep your session ID private — treat it like a password.

---

## Installation & Deployment (App‑style)

Choose Heroku, Render or GitHub Actions.

### 1) Fork the repository
Fork to your account: https://github.com/jayvon33/limkid-X/fork

### 2) Configure environment variables
Set these config vars / secrets on your host:
- SESSION_ID — (required) the session ID you obtained
- OWNER_NUMBER — your WhatsApp number (e.g., +13045593649)
- PREFIX — command prefix (e.g. `!` or `/`)
- PORT — (if required)
- NODE_ENV — `production`

### 3) One-click Deploys
- Heroku: use the button above, supply env vars and deploy.
- Render: use the Render button above and follow deploy steps.
- GitHub Actions: create `.github/workflows/main.yml` (example below) and add secrets to repository settings.

Example GitHub Actions workflow:
```yaml
name: Deploy Limkid-X (CI)

on:
  push:
    branches: [ main ]
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        node-version: [20.x]

    steps:
      - uses: actions/checkout@v3
      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node-version }}
      - name: Install dependencies
        run: npm install --legacy-peer-deps
      - name: Start
        run: npm start
```

### 4) Run locally
1. Clone your fork:
   - git clone https://github.com/<your-username>/limkid-X.git
2. Install:
   - npm install
3. Create a `.env` with required values (or use environment variables)
4. Start:
   - npm start

---

## Quick Commands (examples)

- /help — Show list of commands and usage
- /sticker <image> — Convert image to sticker
- /ban @user — Ban a user (group admin only)
- /welcome on|off — Toggle welcome messages
- /setprefix <char> — Change bot command prefix (owner only)

(Replace with the full command list from your bot's code — consider adding a Commands.md later.)

---

## Contact & Community

All clickable social badges below open the corresponding link or chat.

- Telegram (Developer / Support):  
  [![Telegram](https://img.shields.io/badge/Telegram-@jayvonkid-26A5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/jayvonkid)

- Telegram (Group / Channel):  
  [![Telegram Channel](https://img.shields.io/badge/Telegram-Channel-26A5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/jayvonkid)

- Instagram:  
  [![Instagram](https://img.shields.io/badge/Instagram-@jayvon306-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/jayvon306)

- WhatsApp (Owner):  
  [![WhatsApp](https://img.shields.io/badge/WhatsApp-%2B1%20(304)%20559-3649-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/13045593649)

- WhatsApp (Support):  
  [![Support WhatsApp](https://img.shields.io/badge/Support-%2B233%2050%20431%204086-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/233504314086)

Other links:
- Repo (Limkid‑X): https://github.com/jayvon33/limkid-X  
- Fork this repo: https://github.com/jayvon33/limkid-X/fork  
- Issues / Bug Reports: https://github.com/jayvon33/limkid-X/issues

Phone numbers (plain text):
- Owner WhatsApp: +1 (304) 559-3649  
- Support (WhatsApp): +233 50 431 4086

---

## Screenshots & Demo

Add screenshots or short GIFs showing:
- Pairing flow (pair site & QR)
- Example bot responses in a group
- Sticker/media conversion examples

---

## Security & Privacy

- Keep your SESSION_ID secret and store it in Config Vars or Secrets.
- Do not share your session ID publicly.
- Use responsibly and follow WhatsApp Terms of Service.

---

## Contributing

We welcome contributions:
1. Fork the repo
2. Create a feature branch
3. Open a PR describing your change
4. Add tests and documentation for new features

For plugin authors: add a plugin folder with README, example commands, and export an init function the bot loads.

---

## License

This repository currently has no license file. Add a LICENSE (e.g., MIT) if you want others to reuse your code.

---

Thank you for using Limkid‑X — deploy fast, manage smarter, and customize your WhatsApp experience.   
   
  2..DEPLOY ON RENDER ⤵️

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/jayvon33/Limkid-X.git)


   3..DEPLOY ON GITHUB ⤵️


</details>

<b><strong><summary align="center" style="color: Yello;">Deploy On Workflow</summary></strong></b>
<p style="text-align: center; font-size: 1.2em;">
 
<h8>Copy the workflow codes and then frok the repo edit config add session id then save and now click on repo action tag then click on start new workflow then paste workflow codes rename main.yml to deploy.yml and save the file</h8>
<h3 align-"center"> Important</h3>
<h6 align-"center">Attention! We do not take responsibility if your github account is suspended through this Deploy method, I advise you not to use this workflow deploy method in the latest github accounts, github accounts created a year or more ago have not received the risk of suspension so far, this works It will only be done for 6 hours, you need to update the code to reactivate it.</h6>

```
name: Node.js CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:

    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}

    - name: Install dependencies
      run: npm install

    - name: Start application
      run: npm start
```
<a><img src='https://i.imgur.com/LyHic3i.gif'/>

### Thank You Dear

> DEVELOPER OF Limkid-X 
- [LIMKID-X ](https://github.com/jayvon33)
- Creater and Owner Of Limkid-X 

> Limkid-X Helper
- [LIMKID-X](https://github.com/jayvon33)
- For helping in bot plugin files.
---
<a><img src='https://i.imgur.com/LyHic3i.gif'/># Limkid-X 
