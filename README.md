# ForgeDesk

**Minecraft servers, without the terminal.** ForgeDesk installs, runs and looks after your Minecraft servers (mods, backups and schedules included) in one calm Windows app.

**[Website](https://forgedesk.rosariocampagna.duckdns.org/)** · **[Download the latest version](../../releases/latest)** · **[Release notes](../../releases)**

[![Latest release](https://img.shields.io/github/v/release/RosarioCampagna/ForgeDesk?label=latest&color=3fb28a)](../../releases/latest)
![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%26%2011-3fb28a)

![The ForgeDesk dashboard](https://forgedesk.rosariocampagna.duckdns.org/assets/img/dashboard.webp)

> This repository only hosts the **releases**. The source code is not published. ForgeDesk is not affiliated with or endorsed by Mojang Studios or Microsoft.

## Contents

- [What it does](#what-it-does)
- [Download and install](#download-and-install)
- [Good to know](#good-to-know)
- [Your data and your keys](#your-data-and-your-keys)

## What it does

### Create and run servers

- **Vanilla, Fabric, Forge and NeoForge**, with Forge all the way back to Minecraft 1.5.2. Pick a version and ForgeDesk installs it.
- **Java is handled for you.** It uses the Java already on your PC, or downloads the one a server needs (Temurin, Zulu or Mojang's own, your choice). A server runs on exactly the Java its Minecraft version was made for, because a newer one can stop it from starting. You never pick a path unless you want to.
- **Start, stop and restart** from a server's page, with a live **console** and a command box, and **TPS, CPU, memory and uptime** charts. Memory can be Auto or a size you choose; you can also set the Java, extra JVM arguments and environment variables per server.
- **Server settings** (`server.properties`) as a form, checked as you type, with each setting explained.
- **When a server crashes, it says why in plain words**: out of memory, a Java that is too old for the server, and other common causes, read from the console, the log and the crash report. A server that ran out of memory but is still running gets a warning too.
- **Can friends join?** A Connect card shows the address to share and checks whether this PC and your network can reach the server. On a router that allows it, one button asks the router to open the port (UPnP), and another closes it again.
- **Warns when two servers use the same port**, and keeps each server's own icon (a block you pick, or a modpack's picture, shown here, on your phone and in the game's server list).

### Mods and modpacks

![Mods tab](https://forgedesk.rosariocampagna.duckdns.org/assets/img/mods.webp)

- **Browse Modrinth and CurseForge side by side**: search, sort, filters for version, loader and category, and a version picker. The filters follow the server you are installing to, so you only see what fits.
- **Dependencies come along**, and removing a mod warns you what needs it. When a Modrinth pack makes a server, the mods it marks as game-client-only are left out.
- **Updates are always a deliberate click.** ForgeDesk checks for newer versions when a server's page opens and lists the mods that have one first.
- **Modpacks make a new server.** Pick a pack (Modrinth or CurseForge) and press Create server: ForgeDesk reads the pack, installs the loader and the Minecraft version, downloads its files (checking each one) and applies its configuration. The pack shows above the mod list with its picture, version and a link.
- **Update a modpack in place** to another version, with a live row that says what it is doing (the backup, each download, the replacement). **Repair** puts back missing or changed files of the installed version. A switch (off by default) lets you update or remove the pack's mods one by one instead.
- **Export a client pack** of a server's Modrinth mods for your players, so they can install the same ones.

### Files and worlds

![Files tab](https://forgedesk.rosariocampagna.duckdns.org/assets/img/files.webp)

- **A file manager for each server**: browse the folder, drag files in from Explorer, make folders, rename, and open small text files (settings, logs, configs) to read and edit. Saving keeps the old text beside the file as `.bak`, and a file that changed on disk meanwhile is never overwritten without asking.
- **Delete goes to the Recycle Bin**, after a question that says what and how big. What the server needs to start asks for a second, typed confirmation. A running server's world, jar, libraries and log cannot be touched.
- **Select several files** with the tick-box button: Shift-click for a range, Ctrl+A for all, F2 to rename, Delete to delete.
- **Worlds:** drop a world (a zip or a folder) on the tab to replace the server's, with a backup taken first. **Start a new world** under a name you choose (with an optional seed) and the old one stays exactly where it is. **Use this world** switches to any world folder, including the old one.

### Players

![Players tab](https://forgedesk.rosariocampagna.duckdns.org/assets/img/players.webp)

- See **who is online** and, for everyone who has played, what the world saved about them: health, food, level, game mode, position, play time, deaths and inventory, with a copy-ready `/tp` command.
- **Act on a player from their page**: change game mode, heal, feed, kill, make operator, whitelist or ban, with a question first where it matters.
- **Give item**: pick an item from a picture grid and ForgeDesk gives it safely. It saves the world, reads the inventory, gives only what fits, and tells you what the server answered. Technical items are offered only to players in Creative. Works for Minecraft 1.13 up to 26.3.
- **Item pictures are opt-in**: they come from Mojang's own files and are fetched only if you agree. Player heads come from Mojang's skin servers and can be switched off in Settings.

### Backups

![Backups page](https://forgedesk.rosariocampagna.duckdns.org/assets/img/backups.webp)

- **Manual or scheduled backups**, with a number to keep, **hash-checked when made and again before any restore**.
- **A restore always takes a safety backup of the current state first**, and is staged so a failure does not leave a half-restored server.
- Works on a running server (ForgeDesk tells it to stop saving, saves, copies and then lets it save again). A backup of a running server is best effort; for a fully consistent copy, stop the server first.

### Automation

![Schedule tab](https://forgedesk.rosariocampagna.duckdns.org/assets/img/schedule.webp)

- **Rules that read like sentences.** Pick *when*: a time of day on chosen days, every N minutes or hours, or something that happens in the game (a player joins or leaves, a player dies, down to one cause or one mob). Pick *what*: restart (with warnings at 5 minutes, 1 minute and 10 seconds), back up, say a message (one of several phrases, never the same twice in a row) or run a command.
- **Messages when something goes wrong or happens**, in Windows, in Discord or in Telegram: a crash, a failed backup, a player who joined. You write the words for each.
- **Close the window and the server keeps going.** ForgeDesk lives in the system tray, with a summary on hover and a small dashboard on click, and can start with Windows.

### Remote view: check on it from the couch

![Remote view on a phone](https://forgedesk.rosariocampagna.duckdns.org/assets/img/phone-overview.webp)

- A small web page you switch on, off by default. **Pair a phone with a QR code**, or any other browser with a short code.
- See every server, who is online, their inventories, the backups and (if you allow it) the console.
- **You choose what each device may do.** A new device can only look. Raise it to *moderator* (kick, ban, game mode) or *admin* (also start, stop, restart and change schedules), and lower or remove it any time. Every action is written down with the device that made it.
- **Nobody is dropped by surprise.** Stopping or restarting with players online asks first: warn them in the game with a countdown, or stop now.
- No typed commands from a device: it gets a short list of ready-made ones. Everything else stays on the PC.

### Looks, help and updates

- **Dark, deep-black OLED or light**, six accent colours, block pictures drawn simply or in detail, and an aurora that moves, or stands still if you prefer (it follows Windows' "reduce motion" unless you tell it not to).
- **A Help page with guides** (start a new world, add a mod, back up and restore). A guide takes you to the right screen, dims everything else and lets only the control to press answer clicks. First-time tips appear once where something is not obvious.
- **Updates itself, carefully.** ForgeDesk looks for a new version and asks before installing. Updates are signed, and the app refuses anything without a valid signature. An update is refused while a server is running, so nothing is cut off mid-game.

## Download and install

1. Open the **[latest release](../../releases/latest)** and download `ForgeDesk_<version>_x64-setup.exe`.
2. Run it. It installs for your Windows user only and needs no administrator rights.
3. Windows needs the **WebView2 runtime**, which Windows 11 and current Windows 10 already include.

The installer is **not yet signed with a Windows code-signing certificate**, so SmartScreen may show "Windows protected your PC". Choose **More info**, then **Run anyway**. You can check the download against `SHA256SUMS.txt` on the release page.

**Requirements:** Windows 10 or 11 (64-bit). Java is not bundled: ForgeDesk uses one already on your PC or downloads the one a server needs.

## Good to know

- **Windows only.** It uses the Recycle Bin, Explorer, the tray and the Windows installer.
- **CurseForge needs your own API key**, entered in Settings. Modrinth needs nothing. Not every CurseForge modpack can be installed automatically: a pack whose files the author does not allow outside CurseForge gets an explanation instead.
- **The Remote view page is plain HTTP and not encrypted.** Keep it on your home network, or behind Tailscale or an HTTPS proxy; behind HTTPS, type that address in Settings, Remote view, and the pairing QR code points there.
- **Opening a router port (UPnP)** works only on routers that allow it. The Remote view's own port is never opened.
- **Notifications** are sent only while ForgeDesk is running, so a crash while it is closed cannot be announced.
- The crash explanation recognises a list of common causes; for the rest it shows the game's own words.

## Your data and your keys

- **Local-first.** Your servers, worlds and settings stay on your PC. There is no account to make.
- **Keys stay locked.** A CurseForge key, a Discord webhook or a Telegram token lives in the Windows Credential Manager, never in a file or a log.
- **Downloads come only from a short list of hosts** (Mojang, the loader projects, Modrinth, CurseForge, the Java sources you choose), and files are checked against their published hashes.
- The server's folder is the only place the file manager can reach, and ForgeDesk's own files in it cannot be changed from there.

## About

ForgeDesk is built with Tauri, Rust and React; the installer is about 7 MB. Minecraft belongs to Mojang Studios and Microsoft, and the item pictures in the screenshots are Mojang's artwork. Modrinth and CurseForge and their marks belong to their owners. The pixel lettering is Monocraft by Idrees Hassan (SIL Open Font License 1.1); the text is set in Inter (SIL OFL 1.1).

**[forgedesk.rosariocampagna.duckdns.org](https://forgedesk.rosariocampagna.duckdns.org/)**
