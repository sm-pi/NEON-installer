# Troubleshooting

[← Back to the README](../README.md)

Neon keeps a record of what it heard and did in **`%APPDATA%\Neon\neon.log`**. To open it, press **Win + R**, paste `%APPDATA%\Neon\neon.log` and press Enter. It's the first place to look, and useful to include when you [report a problem](https://github.com/sm-pi/NEON-installer/issues/new/choose).

## Installing

**Windows says "Windows protected your PC".**
The installer isn't code-signed yet, so Windows doesn't recognise it. Click **More info**, then **Run anyway**. If you want to be sure the files are genuine, [check their hashes](INSTALL.md#download) first.

**Setup asks for `install-2.bin` (or another part), or says a file is damaged.**
Every `.bin` file must be in the same folder as `install.exe`. If they are, one file probably didn't download completely: compare its hash with `SHA256SUMS.txt` and download it again.

**There isn't enough disk space.**
Neon needs about 14 GB on the drive with your user folder (usually `C:`). Free some space, or choose another drive on setup's *Select Destination Location* page.

**My antivirus blocks setup or Neon.**
Some antivirus programs distrust new, unsigned programs. If you downloaded Neon from this page and the hashes match, allow it in your antivirus.

## Listening and understanding

**Neon doesn't wake up.**
- Say **"Neon"** clearly, then your request. *"Hey Neon"* also works.
- Click the orb to make it listen without the wake word.
- In **Settings > Wake word and listening**, add your own way of saying "Neon".
- Check the microphone: **Settings > System > Sound > Input** in Windows should show the bar moving when you speak.

**Neon mishears me.**
Say **"Neon, learn my accent"** and read the sentences it shows (about 3 minutes). Neon learns how it mishears you and switches to the speech model that understands you best. In **Settings > Understanding you** you can also choose the larger speech model, which is better with accents.

**Neon says a microphone gives no sound.**
The microphone may be muted, unplugged or blocked. In Windows, open **Settings > Privacy & security > Microphone** and make sure *Microphone access* and *Let desktop apps access your microphone* are on.

**Neon wakes up when nobody called it.**
It can happen with a TV or video playing nearby. Neon ignores stray words it can't act on. If it happens often, move the microphone away from the speakers, or use a headset.

## Speed

**The first request is slow.**
Neon prepares its models the first time, which takes a few seconds. Later requests are answered in about a second. After a long quiet period, Neon frees memory and the next request is a little slower again.

**Neon is slow on my PC.**
On PCs without a graphics card that has 6 GB or more of its own memory, Neon uses its lighter model set and runs on the processor. Most commands are still quick; long writing tasks take longer. Closing heavy programs, especially browser tabs, helps.

**Neon uses a lot of memory.**
Neon's models need memory to run, and it frees the big ones when you haven't used them for a while. You can switch off abilities you don't use in **Settings > What Neon may do**.

## Doing things

**Neon can't find an app I asked for.**
Say the name as it appears in the Start menu, for example *"open Visual Studio Code"*. If Neon still can't find it, it tells you.

**Messaging doesn't work.**
Sign in to WhatsApp Web, Messenger, Facebook, Instagram or Telegram Web in your browser first, and keep that tab open. Neon reads each message back and sends it only when you say *"yes"*.

**Neon typed into the wrong place.**
Say *"undo"* straight away. Clicking the box you want before you ask also helps Neon find it.

## Voice security

**Neon doesn't recognise my voice.**
A cold or a noisy room can change your voice. Neon then asks for your password, then your recovery password. If it happens often, turn security off with your password and set it up again in a quiet room.

**I forgot my passwords.**
For your safety, passwords can't be recovered. If voice security is on and you can't pass it, uninstall Neon, delete the `%APPDATA%\Neon` folder (this also removes your settings and what Neon learned) and install Neon again.

**The PC shut down after three wrong tries.**
That's the breach protection. To make Neon only lock the PC instead, open **Settings > Security**.

## The orb

**The orb is missing.**
Start Neon from the Start menu, or find its icon in the taskbar's notification area (click **^** if it's hidden). The orb may also be set to show only while Neon is talking (**Settings > Orb**).

---

Still stuck? [Open an issue](https://github.com/sm-pi/NEON-installer/issues/new/choose) with what you said, what Neon did, and the relevant lines from `neon.log`.
