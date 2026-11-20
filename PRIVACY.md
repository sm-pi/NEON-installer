# Privacy

[← Back to the README](README.md)

**Neon runs entirely on your computer.** It has no account, no cloud service and no telemetry. What you say is turned into text on your PC, understood on your PC and acted on by your PC.

## What goes online, and when

Neon itself never sends what you say, what it learns or anything about you to the internet. It uses the internet only when **you ask it to do something online**: open a website, search the web, or use a web app such as WhatsApp Web, Google Docs or YouTube in your browser. Those sites then work exactly as if you used them yourself, under their own privacy policies.

## What Neon stores

Everything is kept in your own Windows user folder, **`%APPDATA%\Neon`**, and nowhere else:

| File | What it holds |
|---|---|
| `settings.json` | Your settings and the name Neon calls you |
| `notes.md` | Notes you asked Neon to take |
| `activity.json`, `learned.json` | What Neon learned from your requests: how you phrase things and what you do often |
| `router-agent-personal.json` | Neon's understanding of your phrasings (only if you've taught it) |
| `accent.json` | Corrections for words Neon mishears in your accent |
| `users.json` | Voice security, if you set it up: a voiceprint per user (numbers describing a voice, not a recording), and passwords in scrambled form that can't be turned back into the password |
| `hardware.json` | Your PC's memory and graphics, so Neon can choose its models |
| `warm\` | A start-up cache that lets Neon's models get ready faster |
| `neon.log` | A record of what Neon heard and did, for troubleshooting |

**Audio** is processed in memory and not saved. The only exception is **"learn my accent"**: Neon records the sentences you read, uses them to compare its speech models on your voice, and deletes the recordings as soon as it has finished.

## Your control

| You want to | Do this |
|---|---|
| Stop Neon learning | Say *"stop learning"*, or switch it off in **Settings > Learning** |
| Delete what Neon learned | Say *"forget what you learned"* |
| Delete your accent corrections | Say *"forget my accent"* |
| Remove voice security | Say *"turn off voice security"* (needs every user's password) |
| Stop an ability completely | Switch it off in **Settings > What Neon may do** |
| Delete everything | Uninstall Neon, then delete the `%APPDATA%\Neon` folder |

## Microphones

While Neon is running, it listens for its wake word, "Neon", using a small model on your PC. Nothing is acted on until it hears the wake word, and nothing leaves your PC. To stop listening completely, right-click the orb and choose **Quit**.

## Children

Neon is not designed for or directed at children, and collects nothing about anyone.

## Questions

Ask in an [issue](https://github.com/sm-pi/NEON-installer/issues/new/choose). Please don't post private information there; issues are public.
