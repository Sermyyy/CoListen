# 🎵 Listen Together

A Spicetify extension that lets you listen to music in sync with your friends in real time — no accounts, no setup, just a 6-character code.

## Features

- 🎧 **Real-time sync** — everyone hears the same song at the same position
- 👥 **Multiple listeners** — not just two people, as many as you want
- 🎮 **Everyone controls** — any member can play, pause, skip or seek
- 🔒 **No account needed** — just install and go
- 🌐 **Works over the internet** — no need to be on the same network

## How it works

1. One person clicks the **Listen Together** button in the top bar and creates a session
2. A **6-character room code** appears — share it with your friends
3. Friends enter the code and join instantly
4. Music syncs automatically for everyone

## Installation

### Prerequisites
- [Spicetify](https://spicetify.app) installed

### Steps

1. Download `listenTogether.js`
2. Copy it to your Spicetify extensions folder:
   - **Windows:** `%appdata%\spicetify\Extensions\`
   - **macOS/Linux:** `~/.config/spicetify/Extensions/`
3. Run:
   ```bash
   spicetify config extensions listenTogether.js
   spicetify apply
   ```
4. Open Spotify — you'll see the 🎵 button in the top bar

### Via Marketplace
Search for **Listen Together** in the Spicetify Marketplace and click Install.

## Usage

**Creating a session:**
1. Click the headphones icon in the top bar
2. Enter your name
3. Click **Create session**
4. Share the 6-character code with your friends

**Joining a session:**
1. Click the headphones icon in the top bar
2. Enter your name
3. Type the code your friend shared
4. Click **Join session**

**During a session:**
- The room code stays visible so more friends can join at any time
- Everyone can play, pause, skip and seek
- Closing the panel does **not** disconnect you — a mini bar shows the session is still active
- Click **Leave session** to disconnect

## Technical details

- Built with vanilla JavaScript + Spicetify API
- Uses WebSockets via a Cloudflare Worker for real-time relay (free, always on, no cold starts)
- Host broadcasts playback state every 2 seconds to all guests
- Guests can send playback commands back to the host

## Author

Made by [@Sermyyy](https://github.com/Sermyyy)

## License

MIT
