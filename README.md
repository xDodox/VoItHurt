# VoltHurt

A Custom UI for SirHurt V5 built with Tauri v2, React, and Rust. Replaces the default SirHurt UI

## What it does

- Downloads and manages SirHurt V5 core files directly from sirhurt.net
- Injects into Roblox and watches for confirmation via debug log
- Monaco editor with Luau syntax highlighting and autocomplete
- Tab-based script editor — open multiple scripts at once
- Script hub pulling from rscripts.net
- Autoexec support — scripts run automatically after each injection
- Roblox console output forwarded to the built-in terminal via Lua HTTP relay
- Discord RPC
- All settings and session data saved to `%AppData%\VoltHurt`

## Stack

- **Tauri v2** — app shell, file system, window management
- **React + Vite** — frontend
- **Monaco Editor** — script editor
- **Rust** — all backend logic (injection, downloads, HTTP server, Discord IPC)
- **Tailwind CSS** — styling

## Installation

You need [Rust](https://rustup.rs), [Node.js](https://nodejs.org), and [pnpm](https://pnpm.io).

```bash
pnpm install
pnpm tauri build
```

For development:

```bash
pnpm tauri dev
```

## Setup after first launch

1. Go to the Welcome tab and click **Download** — this pulls SirHurt from sirhurt.net
2. Launch Roblox
3. Click **Attach** once you're in a game

VoltHurt writes files to `%AppData%\VoltHurt`. Add that folder to Windows Defender exclusions or the DLL will get flagged.

## Discord RPC

Uses your own Discord application. Set the `client_id` in `commands.rs` and upload a `volthurt` image asset in the Discord Developer Portal if you want the large image to show.

## Notes

- Tested on Windows 11 only
- Requires SirHurt V5 — won't work with other execs
- The auto-updater checks `github.com/xDodox/VoltHurt/releases/latest` — replace with your own repo if you fork this

## License

Do whatever you want with it.
