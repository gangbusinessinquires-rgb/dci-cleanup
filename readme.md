# dci-cleanup

A Python tool to find and leave inactive Discord servers. It scans all servers your account is in, identifies ones where you haven’t sent a message in a configurable number of days, and lets you choose which ones to leave — one by one.

## Features

- Scans all your Discord servers for inactivity
- Configurable inactivity threshold (default: 30 days)
- Interactive prompt — you decide which servers to leave
- Shows live progress and last activity date during scanning

## Requirements

- Python 3.8+
- A Discord user token (not a bot token)

## Installation

```bash
git clone https://github.com/dcistudios/dci-cleanup.git
cd dci-cleanup
pip install -r requirements.txt
```

## Configuration

Copy the example env file and fill in your values:

```bash
cp .env.example .env
```

Edit `.env`:

```env
DISCORD_TOKEN=your_discord_token_here
INACTIVE_DAYS=30
```

- `DISCORD_TOKEN` — Your Discord user token
- `INACTIVE_DAYS` — Number of days without activity before a server is considered inactive (default: `30`)

> ⚠️ **Never share your Discord token.** It gives full access to your account. Keep your `.env` file out of version control (it’s already in `.gitignore`).

## Usage

```bash
python discord_cleanup.py
```

Or use the provided shell script:

```bash
bash clean.sh
```

The tool will:

1. Log in and scan all your servers
1. Flag any server where you haven’t sent a message within the configured period
1. Prompt you for each inactive server: `Would you like to leave? (y/n)`
1. Leave the ones you confirm

## How to Get Your Discord Token

1. Open Discord in your browser
1. Press `F12` to open DevTools
1. Go to the **Network** tab and filter by `api`
1. Send a message or perform any action
1. Look for a request and find the `Authorization` header in the request headers — that’s your token

> Use this at your own risk. Self-bots violate Discord’s Terms of Service. This tool is intended for personal cleanup only.

## License

MIT
