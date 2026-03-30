# <p align="center">🧹 dci-cleanup</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=38BDF8&center=true&vCenter=true&width=500&lines=Discord+Server+Cleanup+Tool;Scan+%7C+Review+%7C+Leave;Declutter+Your+Discord+Account;Built+by+DCI+Studios" />
</p>

-----

## 👋 What is dci-cleanup?

**dci-cleanup** is a lightweight Python tool that scans all Discord servers your account is in, identifies ones you’ve been inactive in, and lets you leave them — one by one, interactively.

> ⚠️ This tool uses a **Discord user token**, not a bot token. Use responsibly and at your own risk. Self-bots violate Discord’s Terms of Service.

-----

## ⚙️ Features

- 🔍 Scans all servers for inactivity
- ⏱ Configurable inactivity threshold (default: 30 days)
- 🖱 Interactive prompt — you choose which servers to leave
- 📅 Displays last activity date per server
- 📡 Live scan progress shown in status

-----

## 🚀 Getting Started

### Installation

```bash
git clone https://github.com/dcistudios/dci-cleanup.git
cd dci-cleanup
pip install -r requirements.txt
```

### Configuration

```bash
cp .env.example .env
```

Edit `.env`:

```env
DISCORD_TOKEN=your_discord_token_here
INACTIVE_DAYS=30
```

|Variable       |Description                                   |Default |
|---------------|----------------------------------------------|--------|
|`DISCORD_TOKEN`|Your Discord user token                       |Required|
|`INACTIVE_DAYS`|Days without activity before flagging a server|`30`    |

-----

## 🖥 Usage

```bash
python discord_cleanup.py
```

Or via the shell script:

```bash
bash clean.sh
```

The tool will:

1. Log in and scan all your servers
1. Flag servers where you haven’t sent a message within the threshold
1. Prompt you for each inactive server: `Would you like to leave? (y/n)`
1. Leave the ones you confirm

-----

## 🔑 How to Get Your Discord Token

1. Open Discord in your browser
1. Press `F12` to open DevTools
1. Go to the **Network** tab and filter by `api`
1. Perform any action (send a message, switch channels)
1. Find a request and copy the `Authorization` header value

> 🔐 Never share your token. It grants full access to your account.

-----

## 🧠 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,linux,github" />
</p>

```
Python
discord.py
python-dotenv
Shell
```

-----

## 🌐 Official Links

<p align="center">
  <a href="https://dcistudios.xyz">
    <img src="https://img.shields.io/badge/DCI_Studios-Website-38BDF8?style=for-the-badge" />
  </a>
  <a href="https://hosting.dcistudios.xyz">
    <img src="https://img.shields.io/badge/DCI_Hosting-Infrastructure-0EA5E9?style=for-the-badge" />
  </a>
  <a href="https://forums.dcistudios.xyz">
    <img src="https://img.shields.io/badge/DCI_Forums-Community-8B5CF6?style=for-the-badge" />
  </a>
  <a href="https://thecarter.xyz">
    <img src="https://img.shields.io/badge/Carter-Portfolio-6366F1?style=for-the-badge" />
  </a>
</p>

-----

## 📬 Contact

<p align="center">
  <a href="mailto:developer@dcistudios.xyz">
    <img src="https://img.shields.io/badge/Email-developer@dcistudios.xyz-D14836?style=flat-square&logo=gmail&logoColor=white" />
  </a>
</p>

-----

## 👑 Leadership

**Owner & Founder:** Carter  
**Organization:** DCI Studios

-----

<p align="center">
<b>DCI Studios — Architecting Excellence.</b>
</p>
