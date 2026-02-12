# Telegram Bot - Sync

A Telegram bot built with Pyrogram for managing plans, gift cards, and various tools.

## Features

- Multiple subscription plans (Plan 1-5)
- Gift card redemption system
- Proxy support
- BIN lookup tools
- VBV checking
- Fake data generation
- Broadcasting system
- User permissions management
- Anti-spam protection

## Setup

1. Install Python 3.12 or higher

2. Install dependencies:
```bash
pip install -r FILES/requirements.txt
```

3. Configure your bot:
   - Edit `FILES/config.json` with your credentials:
     - `BOT_TOKEN`: Your Telegram bot token from @BotFather
     - `API_ID`: Your API ID from https://my.telegram.org
     - `API_HASH`: Your API hash from https://my.telegram.org
     - `OWNER`: Your Telegram user ID
     - `FEEDBACK`: Your feedback channel/username

4. Run the bot:
```bash
python main.py
```

## Project Structure

```
├── main.py              # Main bot entry point
├── FILES/
│   ├── config.json      # Bot configuration
│   ├── requirements.txt # Python dependencies
│   ├── proxy.csv        # Proxy list
│   └── vbvbin.txt       # VBV BIN list
├── BOT/
│   ├── helper/          # Helper modules (start, permissions, etc.)
│   ├── plans/           # Subscription plan handlers
│   ├── tools/           # Utility tools (proxy, gen, bin, etc.)
│   ├── gc/              # Gift card modules
│   └── Charge/          # Payment gateway integrations
├── TOOLS/
│   └── getbin.py        # BIN lookup utility
└── self/                # Self-bot modules
    ├── api.py           # API integrations
    ├── mass.py          # Mass operations
    ├── single.py        # Single operations
    └── tsh.py           # TSH handler

```

## Requirements

- Python 3.12+
- httpx
- requests
- pyrogram
- beautifulsoup4
- flask
- nest-asyncio
- tgcrypto

## Notes

- The bot runs both Pyrogram (Telegram bot) and Flask (web server on port 3000)
- Session files are stored as `MY_BOT.session`
- All plan expiry checks run as background tasks

## Security

⚠️ **Important**: Never share your `config.json` file or bot token publicly!

## License

Private project - All rights reserved
