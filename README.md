<p align="center">
  <img src="assets/neon-logo.jpg" alt="Neon" width="720">
</p>

<h3 align="center">An offline voice assistant for Windows</h3>

<p align="center">
  <a href="https://github.com/sm-pi/NEON-installer/releases/latest"><b>Download</b></a> ·
  <a href="docs/INSTALL.md">Install guide</a> ·
  <a href="docs/USAGE.md">What you can say</a> ·
  <a href="docs/TROUBLESHOOTING.md">Troubleshooting</a> ·
  <a href="PRIVACY.md">Privacy</a>
</p>

---

Say **"Neon"** and ask. Neon opens apps, controls sound and video, browses the web, writes documents, sends messages, manages files, checks your PC and answers questions, all by voice.

**Everything runs on your computer.** Neon uses no online AI service, has no account and sends no telemetry. What it hears, learns and stores stays on your PC.

> This repository holds the **Neon installer and its documentation**. Neon is free to use but **closed source**; see the [licence](LICENSE.txt).

## Highlights

- **Wake word and natural speech.** Say "Neon" from anywhere in the room, then talk normally. Follow-up questions don't need the wake word again. Every connected microphone is used.
- **Fast on any PC.** Most requests are handled by Neon's own small, fast agents in under a second. Larger language models step in only for writing and open questions.
- **Fits your hardware.** Neon checks your PC when it starts and chooses a stronger model set for PCs with a graphics card, or a lighter one for laptops and older PCs.
- **Controls your PC:** apps and windows, volume (system, per app, per video), video playback, tabs and websites, files and drives, downloads and uploads, shutdown and restart.
- **Writes for you:** Google Docs and Sheets, Notepad, letters, emails, reports, research papers, LaTeX, and code in Colab, Kaggle and Jupyter, plus proofreading and "no AI slop" editing.
- **Messages in your browser:** WhatsApp Web, Messenger, Facebook, Instagram and Telegram. Every message is read back and sent only when you say "yes".
- **Works like you do on screen:** it types into the right box on any page and goes through app menus step by step ("download this sheet as PDF").
- **Learns you, locally:** your way of asking, your habits and your accent ("learn my accent"). You can switch learning off or make Neon forget at any time.
- **Voice security:** Neon can take orders only from enrolled voices, with a password and recovery password, multi-user approval and a lock or shutdown after failed attempts.

## Download

Go to the **[latest release](https://github.com/sm-pi/NEON-installer/releases/latest)** and download **every file** in its *Assets* list into **one folder**:

| File | Size | What it is |
|---|---|---|
| `install.exe` | 3 MB | The setup program |
| `install-1.bin` … `install-7.bin` | 1.2–2 GB each, 13.2 GB in total | Neon and its models (setup reads these) |
| `How to install.txt` | | Step-by-step installation guide |
| `How to use Neon.pdf` | | Everything Neon can do and what to say |
| `SHA256SUMS.txt` | | Checksums to verify the download (optional) |

Keep the files together: `install.exe` needs the `.bin` files next to it.

## System requirements

| | Minimum | Recommended |
|---|---|---|
| Windows | 10 or 11, 64-bit | Windows 11 |
| Memory (RAM) | 8 GB | 16 GB or more |
| Graphics | Any, including built-in graphics | A graphics card with 6 GB+ of its own memory |
| Disk space | 14 GB free | SSD |
| Audio | A microphone and speakers | A headset |

No internet connection is needed after downloading. Neon goes online only when you ask it to open a website or use a web app.

## Quick install

1. Double-click **`install.exe`**.
2. If Windows shows *"Windows protected your PC"*, click **More info**, then **Run anyway**. The installer is not yet code-signed.
3. Accept the **licence agreement** and read the third-party notices.
4. Choose your options and click **Install**. No administrator rights are needed.
5. On first start, **type your name**. Neon will call you by it.
6. Say **"Neon, what time is it?"**

The full guide, including uninstalling and moving Neon to another PC, is in **[docs/INSTALL.md](docs/INSTALL.md)**.

## First things to try

| Say | What happens |
|---|---|
| "Neon, open Notepad" | Opens the app |
| "Neon, set the volume to 40" | Changes the volume |
| "Neon, open YouTube" | Opens the website |
| "Neon, write a short poem about rain in a new Google Doc" | Writes it and types it in |
| "Neon, how is my PC doing?" | Checks your processor, memory and disks |
| "Neon, learn my accent" | About 3 minutes of reading to help Neon understand you |
| "Neon, set up voice security" | Neon learns your voice and sets your passwords |

There are many more in **[docs/USAGE.md](docs/USAGE.md)**.

## Verify your download (optional)

In PowerShell, in the download folder:

```powershell
Get-FileHash .\install.exe, .\install-*.bin -Algorithm SHA256 | Format-Table Hash, Path
```

Every hash should match the one in `SHA256SUMS.txt`.

## Documentation

| Document | Contents |
|---|---|
| [Install guide](docs/INSTALL.md) | Requirements, installing, first start, updating, uninstalling |
| [Usage guide](docs/USAGE.md) | Talking to Neon and every kind of command, with examples |
| [Troubleshooting](docs/TROUBLESHOOTING.md) | Common problems and answers |
| [Privacy](PRIVACY.md) | What Neon stores, where, and how to delete it |
| [Changelog](CHANGELOG.md) | What's new in each version |
| [Licence](LICENSE.txt) | The Neon End User Licence Agreement |
| [Third-party notices](THIRD-PARTY-NOTICES.txt) | Open models and libraries included in Neon |

## Support

Found a problem or have an idea? Open an **[issue](https://github.com/sm-pi/NEON-installer/issues/new/choose)**. For a problem, please say what you said, what Neon did, and include the relevant lines from `%APPDATA%\Neon\neon.log`.

## Licence

Copyright © 2026 Sazzad. All rights reserved.

Neon is licensed under the [Neon End User Licence Agreement](LICENSE.txt): you may install and use it on computers you own or control. You may not redistribute, modify or reverse engineer it. Neon includes open models and libraries under their own licences; see [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt).
