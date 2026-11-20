# Installing Neon

[← Back to the README](../README.md)

- [Before you start](#before-you-start)
- [Download](#download)
- [Install](#install)
- [The first start](#the-first-start)
- [Recommended next steps](#recommended-next-steps)
- [What gets installed where](#what-gets-installed-where)
- [Installing on another PC](#installing-on-another-pc)
- [Updating](#updating)
- [Uninstalling](#uninstalling)

## Before you start

| | Minimum | Recommended |
|---|---|---|
| Windows | 10 or 11, 64-bit | Windows 11 |
| Memory (RAM) | 8 GB | 16 GB or more |
| Graphics | Any, including built-in graphics | A graphics card with 6 GB+ of its own memory |
| Disk space | 14 GB free | On an SSD |
| Audio | A microphone and speakers | A headset |

**One installer for every PC.** Neon checks the computer each time it starts. A PC with a graphics card that has 6 GB or more of its own memory and 16 GB or more of RAM gets the **standard** model set. Other PCs, such as laptops and older desktops, get the **lighter** set, which uses less memory and still runs every feature. You don't choose anything.

You do **not** need administrator rights, an internet connection (after downloading), a Microsoft account or any other software. Everything Neon needs is in the installer.

## Download

1. Open the **[latest release](https://github.com/sm-pi/NEON-installer/releases/latest)**.
2. Under **Assets**, download **every** file:
   - `install.exe`
   - `install-1.bin` to `install-7.bin`
   - `How to install.txt`, `How to use Neon.pdf`, `SHA256SUMS.txt`
3. Put them all in **the same folder**, for example `Downloads\Neon`.

The download is about 13.2 GB. If your browser stops a large download part way, download that file again: each `.bin` file is separate.

**Optional: check the files.** Open PowerShell in that folder and run:

```powershell
Get-FileHash .\install.exe, .\install-*.bin -Algorithm SHA256 | Format-Table Hash, Path
```

Each hash must match the line for the same file in `SHA256SUMS.txt`. If one differs, download that file again.

## Install

1. Double-click **`install.exe`**.
2. **"Windows protected your PC"**: this appears because the installer is new and not yet code-signed. Click **More info**, then **Run anyway**.
3. **Licence agreement**: read it and choose **I accept the agreement**. In short, Neon is free to use but closed source: you may not copy, redistribute, modify or reverse engineer it. You can't install without accepting.
4. **Information**: the notices for the open models and libraries Neon includes. Click **Next**.
5. **Options**:
   - *Start Neon when I sign in to Windows* (recommended, so Neon is always ready)
   - *Create a desktop shortcut*
6. Click **Install**. Copying about 14 GB takes a few minutes, depending on your disk.
7. Leave **Start Neon now** ticked and click **Finish**.

If setup says it can't find `install-1.bin` (or another part), the `.bin` files aren't in the same folder as `install.exe`. Move them there and run `install.exe` again.

## The first start

1. A welcome window asks **"What should I call you?"**. Type your name and click **Continue**. Neon greets you by this name from now on. You can change it later in Settings.
2. A glowing circle, **the orb**, appears at the left edge of your screen. It shows what Neon is doing: resting, listening, thinking or speaking. You can drag it anywhere. Right-click it for **Settings**, to hide it, or to quit.
3. Say **"Neon"**, then your request, for example **"Neon, what time is it?"**

The first request takes a few seconds while Neon prepares its models. After that, most requests are answered in about a second.

## Recommended next steps

| Say | Why |
|---|---|
| "Neon, learn my accent" | You read 17 short sentences (about 3 minutes). Neon learns how it mishears you and picks the speech model that understands you best. |
| "Neon, set up voice security" | Neon learns your voice and asks for a password and a recovery password. After that it takes requests only from you, or from people you add. |
| Right-click the orb, then **Settings** | Change the voice, volume, the orb, start-up, what Neon may do, and more. |

All commands are listed in the **[usage guide](USAGE.md)**.

## What gets installed where

| What | Where |
|---|---|
| Neon (program and models) | `%LOCALAPPDATA%\Programs\Neon` |
| Start menu | **Neon**, **How to use Neon**, **Uninstall Neon** |
| Start with Windows (if chosen) | A *Neon* entry under *Settings > Apps > Startup* |
| Your settings, notes, what Neon learned, voice security | `%APPDATA%\Neon` |
| Log of what Neon heard and did | `%APPDATA%\Neon\neon.log` |

Neon installs for your Windows user only. Other users on the same PC install it for themselves.

## Installing on another PC

Copy the **whole folder** with `install.exe` and all the `.bin` files (a USB drive of 16 GB or more works) and run `install.exe` there. No internet connection is needed.

## Updating

Download the new release into an empty folder and run its `install.exe`. Setup closes Neon, replaces the program and models, and keeps your settings, notes, learning and voice security in `%APPDATA%\Neon`. You don't need to uninstall first.

## Uninstalling

1. Open **Settings > Apps > Installed apps** (Windows 11) or **Settings > Apps > Apps & features** (Windows 10).
2. Find **Neon**, then choose **Uninstall**. You can also use **Uninstall Neon** in the Start menu.

This removes the program and models. Your own data in `%APPDATA%\Neon` is kept in case you reinstall. To remove it too, press **Win + R**, type `%APPDATA%`, press Enter, and delete the **Neon** folder.

---

Having trouble? See **[Troubleshooting](TROUBLESHOOTING.md)**.
