# FireForge Command Center

**A free advanced Windows toolkit to debloat, speed up, protect and control Amazon Fire TV and Fire TV Stick devices — no root needed.**

FireForge connects to your Fire TV over your home Wi-Fi using ADB (Android Debug Bridge) and gives you one dark, modern dashboard to switch off Amazon's bloat and tracking, block forced updates, install apps, control the TV from your PC and keep everything the way you set it up.

Every change is reversible. FireForge never deletes Amazon's system files.

> FireForge is free software and is **not affiliated with, endorsed by or sponsored by Amazon**. "Amazon", "Fire TV" and "Fire TV Stick" are trademarks of Amazon.com, Inc. or its affiliates.

---

## Contents

- [Highlights](#highlights)
- [Download & install](#download--install)
- [Getting connected](#getting-connected)
- [Features in detail](#features-in-detail)
- [Safety & undo](#safety--undo)
- [Performance](#performance)
- [Supported devices](#supported-devices)
- [Where FireForge keeps files](#where-fireforge-keeps-files)
- [FAQ & troubleshooting](#faq--troubleshooting)
- [Privacy](#privacy)
- [Licence](#licence)
- [Disclaimer](#disclaimer)

---

## Highlights

- 🖥️ **Three looks, three layouts** – pick one in Settings:
  - **HUD** – holographic cyan on near-black, a sidebar of cut-corner panels with glowing edges, arc gauges and rotating rings around the Health Check score
  - **Wasteland** – rusted, riveted steel and nitro orange, with a wooden **signpost** on the right for getting around (fold it down to icons for more room), stencil lettering and needle gauges
  - **Radiation** – a nuclear bunker console: pages on a green CRT screen, **breaker switches** along the bottom to change section, emergency action switches, a contamination dial and an **incident log** on paper tape
- 🧹 **Debloat** – switch off Amazon services one by one or with one-click presets, from *Safe* to *Extreme*, each with a risk rating. The package, command and tweak lists **update themselves from GitHub**, so new bloatware is covered without updating the app
- ⚡ **Quick Optimize** – faster menus, app pre-compiling, deep storage clean, network tune, background limits and memory saver, all reversible
- 🛡️ **Shields, DNS & VPN** – block forced Fire OS updates, encrypted ad-blocking DNS, ad-tracking and Wi-Fi-scan controls, plus VPN set-up: install WireGuard, send it a config, and switch on always-on VPN with a kill switch
- 📦 **App Store** – 67 popular TV apps installed straight from their official sources, with update checks, plus drag-and-drop APK sideloading
- 🎮 **Remote Control** – a live view of the TV screen, a full remote, typing from your PC, screenshots and screen recording; your keyboard becomes the remote
- 🔁 **Batch & maintenance** – apply a setup to several Fire TVs at once, compare two TVs and copy one's setup to the other, and keep each one tidy on a timer
- 🔄 **After-update check** – when Amazon updates Fire OS, FireForge spots what it switched back on and puts it back in one click
- 🔎 **Quick search** – press **Ctrl+K** to jump to any page, tool, preset, service or app
- 🔔 **Runs in the tray** – minimise to the system tray with Windows notifications; scheduled maintenance keeps going
- 💾 **Backup & Restore** – snapshots of apps and tweaked settings (automatic before big changes), compare, export/import, and APK backups you can reinstall
- ↩️ **Changes & History** – a live list of everything switched off or tweaked on the TV (with one-click revert), and a timeline of every change FireForge made that you can undo
- 🧭 **Setup wizard** – opens straight after installing: pick your look (HUD, Wasteland or Radiation), then it walks you through connecting, a health check and a safe debloat
- 🔔 **Quiet notifications** – results pop up and fade away on their own instead of dialog boxes
- 🩺 **Health Check** – a score with one-click fixes, live CPU, memory, storage and temperature, and a shareable device report
- 🔓 **Root & Recovery** – bootloader/root status, a pre-root checklist and the right guide for your exact model
- 🖥️ **Self-contained** – one installer, no .NET or ADB install needed

---

## Download & install

1. Go to the **[Releases page](https://github.com/FireForgeOffical/FireForge-Command-Center/releases/latest)**.
2. Download **`FireForge-Setup-x.y.z.exe`**. It installs FireForge with a Start-menu shortcut and an uninstaller.
3. Run it. If Windows SmartScreen shows "Windows protected your PC", click **More info → Run anyway**. New apps get this warning until enough people have downloaded them.

**Requirements:** Windows 10 or 11 (64-bit), and the PC and Fire TV on the same network. Everything else, including ADB, is built in.

**Only download FireForge from this GitHub page – it's always free.** Each release lists SHA-256 checksums; to check your
download, run `Get-FileHash <file> -Algorithm SHA256` in PowerShell and compare. The **About** page also tells you whether
your copy is an official release.

FireForge checks GitHub for a new version every time it starts (you can turn this off in **Settings**) and offers to download the installer when one is available.

---

## Getting connected

1. On the Fire TV, open **Settings → My Fire TV → About** and click **your device name 7 times** until it says you're a developer.
2. Go back to **My Fire TV → Developer Options** and switch **ADB Debugging** on.
3. Find the TV's IP address under **Settings → My Fire TV → About → Network** (for example `192.168.0.18`).
4. In FireForge, type the IP in the top bar and press **Connect** — or press **Scan Network** to find Fire TVs on your network. If it finds more than one, you pick which to connect to (devices you've used before show their saved names).
5. The first time, the TV asks *"Allow USB debugging?"* — tick **Always allow from this computer** and press **OK** with the remote.

The first time you start FireForge, a **setup wizard** walks you through these steps, runs a health check and offers a safe debloat preset. You can run it again from **Settings → Connection**.

FireForge remembers each device you connect to (see **Devices ▾** in the top bar), reconnects to the last one on start-up, and reconnects automatically if the connection drops — if Wi-Fi blips in the middle of a long operation, it reconnects and carries on where it left off.

---

## Features in detail

The sidebar is grouped into **Overview** (Dashboard, Health Check, Benchmark), **Clean Up**, **Apps**, **Device**, **Safety & Undo** and **Advanced**, with **Settings** and **About** pinned at the bottom. Debloat Engine, Backup & Restore and Changes & History have tabs along the top. Press **Ctrl+K** to jump anywhere. When something finishes successfully, a small notification slides in at the bottom-right instead of a box you have to click away; only problems still stop you with a message.

Before an option changes something on your Fire TV, FireForge tells you what will happen and how to undo it. When a preset or selection includes a service that's risky to switch off (the home screen, Appstore, WebView, account sign-in, voice), it says what will stop working, with an extra warning on Fire OS versions where it's riskier, such as the 2022 updates that block other launchers from replacing the home screen. Presets and debloats also show how much memory the apps you're switching off are using right now. You can switch these warnings off in **Settings → Safety**; removing apps, presets and other big changes always ask.

### 📊 Dashboard

- **Live** tiles with mini graphs, updated every few seconds while the page is open: CPU load, memory, temperature, network download/upload speed, Wi-Fi signal strength, the app on screen right now, free storage and uptime
- **Device details** in four tidy cards – Device, Status, Storage & Memory, and Display & Network – with each value on its own row (hover to see anything cut off)
- **Quick Actions** across the top: refresh, reboot, recovery, bootloader, shut down, sleep, restart the home screen, stop background apps, clear caches and a shortcut to Remote Control (each asks first, and hovering explains what it does)

### 🩺 Health Check

- **Run Health Check** gives a score with a list of issues and **one-click fixes**, then **Fix Recommended Issues** fixes the safe ones in one go
- The apps using the most memory right now (live CPU, memory, storage and temperature are on the Dashboard)
- **Export Device Report** – a one-page HTML summary of the device (model, Fire OS, storage, memory, every disabled or removed app, and the state of each shield). Print it to PDF from your browser. Serial number, MAC address, IP and Wi-Fi name are left out so it's safe to share.

### ⏱️ Benchmark

- Times how fast a few of your apps open from cold and records free memory, free storage, running processes and how many apps are switched on
- **Run Before** while the Fire TV is still stock, debloat and optimize, then **Run After & Compare** – the results table shows both runs side by side with the change (green better, amber worse)
- Results are kept per TV; **Copy Results** puts them on the clipboard to share

### 🧹 Debloat Engine

**Presets tab**
- 22 one-click bundles graded **Safe**, **Recommended**, **Aggressive** and **Extreme**: privacy, ad blocking, OTA blocking, media-only, gaming, custom-launcher prep, casting shutdown, quiet mode, kiosk and more
- Search and filter by severity; restore any preset just as easily
- **Apply to Several Devices** jumps to Batch Mode on the Extra Tools page

**All Services tab**
- 72 Amazon services in 10 categories (telemetry and crash logs, OTA updates, ads and promotions, built-in Amazon apps, Alexa, screensavers, kids' controls, casting and remote apps, speech, and core OS services), each with a description and risk rating
- Settings, the keyboard and the package installer are deliberately left out, because disabling them can lock you out of the device
- Filter by risk, search by name or package, tick what you want, then **Disable**, **Remove** or **Restore**
- **Export / Import profiles** (`.fireforge.json`) to reuse your picks on another stick or share them
- If Fire OS refuses to disable something, FireForge offers to remove it for the current user instead (backing the APK up first), and remembers which packages are protected so you aren't asked again

### ⚡ Quick Optimize

One-click tune-ups that work on every model:
- **Balanced Boost** – 0.5× animations, stops background apps, clears app caches
- **Maximum Performance** – animations off, telemetry and ad services disabled, ad tracking limited, background Wi-Fi scans off
- **App Speed Compile** – pre-compiles apps so they open faster
- **Deep Storage Clean** – clears every cache, leftover APK installers and the system log, and shows the space you got back
- **Network & Radio Tune** – Wi-Fi never sleeps, background Wi-Fi and Bluetooth scanning off
- **Background Limits** – stops Amazon extras (Photos, Music, Freevee, Silk and others) running in the background
- **Memory Saver** – keeps fewer apps cached so the one you're using gets more RAM (Fire OS 7 and newer)
- **Revert to Stock** – puts everything back, including Network Tune, Background Limits and Memory Saver
- **What's Using Memory & Storage** – every app's memory use right now (stop or switch off any of them) and its app, data and cache size
- **Sleep & Screensaver Timers** – any screensaver start time from 1 minute to never, and a sleep timer from 5 minutes to never (Fire OS has no sleep setting of its own). A few newer models ignore custom timers
- **TV Control over HDMI (CEC)** – switch it on or off, for when the TV keeps turning itself on
- A live **Current State** card shows how the device is tuned right now

### 🛡️ Shields, DNS & VPN

Each card shows the current setting and lets you switch it on or off:
- **Fire OS Update Shield** – stops Amazon pushing system updates that can undo debloating (and can be restored any time)
- **Encrypted Private DNS** – AdGuard, Mullvad, Cloudflare, Quad9, Google or your own provider (for example NextDNS)
- **Interest-based ads**, **connectivity check pings** and **background Wi-Fi scanning**
- A shortcut to the TV's own privacy settings (usage data and content recognition)
- **VPN** – shows which VPN apps are installed and whether a VPN tunnel is up. Get a VPN app from the Appstore, install the official **WireGuard** app and send it a config file from your PC, and switch on **Always-on VPN** and the **kill switch** (blocks the internet whenever the VPN drops)

### 📱 App Manager

- Every installed app with status, type (system or user), size and a risk rating
- Filter, search and sort by any column
- **Disable**, **Enable / Restore**, **Remove** (with an automatic APK backup) and **Clear Data** — one app or many at once
- A storage summary showing how much space apps use
- **Force Off** – for apps Fire OS won't let you switch off. FireForge tries each method in turn until one works: switch off, remove for your user, **suspend** (stays installed but can't open or run), **hide** (rooted devices), and finally **block it from running in the background**. It reports which method worked for each app, and every step can be undone in Changes & History. Presets and debloats offer Force mode automatically when Fire OS refuses both disabling and removing

### 📥 Sideload APKs

- Drag APK files onto the page (or pick them) and install them all in one go
- Failed installs stay in the list with the reason, ready to retry

### 🛍️ App Store

Popular apps, always from the official source, never a mirror site. Apps are grouped into collapsible categories — Streaming, UK TV, Free TV, Kids, Media Servers, Video Players, Music, Games, Screensavers, Web Browsers, Files & Sharing, VPN & Privacy and Utilities — just like the Presets and All Services pages. Click a category to open it, or search, filter by category or show only installed apps and the matching categories open on their own. Each card shows the app's icon, downloaded once from its official website and kept on your PC (apps without one get a tile with their initials).

| Source | Apps | What FireForge does |
|---|---|---|
| Developer's GitHub releases | SmartTube, Jellyfin, Moonfin, Wholphin, Moonlight, Lemuroid, Aerial Views, mpv, Just Player, Nova Video Player, TV Bro, Material Files, LocalSend | Downloads the build that matches your stick's processor, installs it, checks for updates and offers to open it |
| Amazon Appstore | Downloader, VLC, Netflix, YouTube, Disney+, Apple TV, Paramount+, Crunchyroll, Pluto TV, Tubi, Plex, Emby, Stremio, Spotify, X-plore File Manager, Send Files to TV, AirScreen, Analiti Speed Test, Hulu, Peacock, Sling TV, Easy Fire Tools | Opens the app's Appstore page on the TV so you can install it with the remote |
| Amazon Appstore (search) | Max, YouTube TV, Twitch, BBC iPlayer, ITVX, Channel 4, My5, NOW, Red Bull TV, Apple Music, Pandora, TuneIn Radio, Tidal, Deezer, DAZN, Discovery+, STV Player, The Roku Channel, Xumo Play, PBS, YouTube Kids, PBS Kids, Proton VPN, NordVPN, Surfshark, ExpressVPN, AnyDesk | Opens an Appstore search for the app on the TV |
| Developer's website | Kodi, RetroArch, Dolphin, PPSSPP, Mouse Toggle | Opens the official download page |

After installing **Aerial Views**, FireForge can set it as the Fire TV screensaver (normally only possible with ADB commands).

### 🎮 Remote Control

- **Live view** of the TV screen next to a full remote: d-pad, Back, Home, Menu, rewind / play-pause / fast-forward, volume, mute, sleep, wake and Settings
- **Type on the TV** – send text to the selected box (much faster than the on-screen keyboard for passwords and URLs), plus Delete and Enter keys
- **Save Screenshot** to your Pictures folder
- **Record** the TV screen (up to 3 minutes per clip), saved as MP4 to `Documents\FireForge\Recordings`. Protected video such as Prime Video or Netflix records as black, and a few older models don't support recording.
- **Keyboard control** – while this page is open, use the arrow keys, Enter, Backspace (Back), Home and Space (play/pause)

### 📁 File Transfer

- Browse the Fire TV's storage
- Drag files from your PC to upload them, or download files back to the PC
- Create folders and delete files

### 💾 Backup & Restore

Two tabs:

**Snapshots**
- Record which apps are disabled or removed **and** every tweaked setting (animations, ad tracking, scanning, Private DNS, Wi-Fi sleep, Memory Saver)
- Leave the name empty for an automatic name (model + date)
- **Automatic snapshots** are taken before presets, debloats, removals, Maximum Performance and snapshot restores (the last 10 per device are kept; switch off in Settings → Safety)
- **Compare with Device** (or double-click) shows exactly what a restore would change, before anything happens
- **Restore** puts apps and settings back to how they were
- **Export / Import** snapshots to move them to another PC or share a setup
- Snapshots from a different Fire TV are shown in amber

**APK Backups**
- Every app FireForge saved to your PC before removing it, with size, date and whether it's on the connected TV now
- **Reinstall Selected** brings an app back the normal way, or installs the saved APK if that doesn't work
- **Delete Selected** frees space on your PC

### ↩️ Changes & History

Two tabs:

**Applied Now**
- Reads the connected Fire TV live and lists everything that differs from Amazon's defaults: disabled apps, removed apps, and active tweaks (animations, ad tracking, connectivity pings, Wi-Fi/Bluetooth scanning, Wi-Fi sleep, Memory Saver, Private DNS, Background Limits, resolution and density overrides, custom home screen)
- Includes changes made by other tools or before you used FireForge
- Each row shows its category and impact; filter and search the list
- **Revert Selected** puts any row back to the default; **Export List** saves it as CSV or text

**History**
- A timeline of everything FireForge changed on each Fire TV: apps disabled, removed or restored, settings and display changes — with the old and new values
- **Undo Selected** reverses individual changes; **Undo Whole Operation** reverses everything a preset, batch or fix did in one go
- Filter to the connected device, or see every device; clear the history when you no longer need it
- Recording can be switched off in **Settings → Safety**

### 🧰 Extra Tools

**Apps & display**
- Launch or force-stop any installed app
- **Custom launcher** – install a third-party home screen, try to make it the default, or go back to Amazon's
- TV shortcuts: Fire TV settings, network settings, developer options and restart the home screen
- Interface animation speed, display resolution and screen density (DPI) overrides

**Batch & maintenance**
- **Batch Mode** – pick a preset or profile, Balanced Boost and/or the privacy shields, tick your saved Fire TVs, and FireForge applies it to each one in turn, then reconnects to the device you started on
- **Scheduled Maintenance** – every 1–24 hours while FireForge is open: clears caches, stops background apps, puts shield settings back, and re-disables or re-removes apps that an Amazon update switched back on. It compares against a saved baseline for each device. It can also **restart the Fire TV every night** at a time you choose.
- **After-Update Check** – compares the TV with everything FireForge changed (and the maintenance baseline) and lists apps that came back and settings that reset, ready to put back in one click. It runs automatically when FireForge sees a new Fire OS version.
- **ADB-only App Permissions** – pick an installed app (button remappers, mouse cursors, automation tools) and FireForge grants the permissions that normally need a computer, including turning on its accessibility service. **Take Back** removes them
- **Compare Two Fire TVs** – reads two saved TVs and shows every difference in apps and tweaked settings, then makes one match the other (a snapshot is taken first)

### 🔓 Root & Recovery

FireForge **never** runs exploits, roots or flashes anything automatically — that's model-specific and doing it blindly can brick a device. Instead it:
- Detects the model and codename, Fire OS and Android version, security patch, **bootloader lock state**, **root (Magisk)** and **SELinux**
- Shows a **pre-root checklist**: firmware noted, updates blocked, snapshot taken, fastboot available
- Opens the right community guide for your exact model, and links to official firmware and the XDA forum
- Reboots to recovery or the bootloader, and checks fastboot status (when `fastboot.exe` is in the adb folder)
- **Root Tools** (rooted devices only): test root access, and disable apps Fire OS refused to switch off
- **Copy Info** puts your device details on the clipboard, ready to paste when asking for help

### 🖥️ Terminal & Logs

- Run your own ADB shell commands
- See everything FireForge does, with timestamps
- Read the Fire TV's own live, colour-coded system log (logcat)

### ⚙️ Settings

- **Connection** – reconnect on start-up, connection watchdog and how often it checks, default ADB port, run the setup wizard again
- **Safety** – warnings before options change the TV, change history on/off, APK backup before removing, automatic snapshots before big changes, confirm before reboot or shut-down, show the terms notice only once, forget the list of protected apps
- **Background & Start-up** – try other saved Fire TVs if the last one doesn't answer, Wake-on-LAN before connecting (Fire TV Cube), minimise to the system tray, Windows notifications, and the after-update check
- **Interface** – theme (**HUD**, **Wasteland** or **Radiation**), **compact layout** for small laptop screens, remember window size, which page opens at start-up, refresh speeds for live stats, logs and the Remote Control view
- **Logging** – timestamps, and saving the log to a file (one per day)
- **Updates** – check on start-up, check now, un-skip versions, release notes, and **Copy Diagnostics** for bug reports. Also keeps the **debloat definitions** (bloatware, commands, tweaks and presets) up to date automatically from GitHub, with a **Check for New Definitions** button
- **Folders** – one-click access to every folder FireForge uses
- **Reset** – forget saved devices, or reset all settings (devices, snapshots, profiles and backups are kept)

---

## Safety & undo

- **Disabled** apps stay on the device and come back with **Restore** on Debloat Engine (either tab) or App Manager.
- **Removed** apps are only removed for the current user — the original stays in the system partition, so **Enable / Restore** in App Manager brings it back. FireForge also saves the APK to your PC first.
- Take a **snapshot** in Backup & Restore before trying Aggressive or Extreme presets (FireForge also takes one automatically).
- Check **Changes & History → Applied Now** to see everything that's currently changed on the TV and put any of it back.
- If something goes badly wrong, a factory reset from the Fire TV's settings returns it to stock.

Disabling some services can stop Amazon features working (for example recommendations, Alexa or the Appstore). Every item shows a risk rating, and the Safe and Recommended presets avoid anything that breaks normal use.

---

## Performance

FireForge is built to stay light:
- Device reads are **batched** – Applied Changes, snapshots, Health Check, Quick Optimize and the Dashboard each read the TV in one or two round trips instead of dozens
- App lists are **cached** for a few seconds and refreshed automatically as soon as anything is installed, removed, enabled or disabled
- Rarely used pages (App Store, Root & Recovery, Remote Control, File Transfer, About) are built the first time you open them, so start-up is quicker
- Live stats, live logs, the live TV view and animations **pause while the window is minimised**
- Lists and card grids are double-buffered (no flicker), and the Terminal keeps its most recent lines instead of growing for ever

---

## Supported devices

FireForge works with Fire TV devices running Fire OS 5, 6, 7 or 8 that have **ADB Debugging** in Developer Options, including:

Fire TV Stick (all generations), Fire TV Stick Lite, Fire TV Stick 4K, Fire TV Stick 4K Max (including the 2023 model, "Karat"), Fire TV Cube, Fire TV boxes and Fire TV Edition smart TVs.

Newer Fire TV devices running **Vega OS** (not Android-based) are not supported. Some packages are protected by Fire OS on newer firmware and can't be disabled without root — FireForge tells you when that happens.

---

## Where FireForge keeps files

| What | Where |
|---|---|
| Settings, saved devices, snapshots, change history | `%AppData%\FireForge\` |
| Log files (if enabled) | `%AppData%\FireForge\Logs\` |
| App Store icons | `%AppData%\FireForge\IconCache\` |
| APK backups | `Documents\FireForge\APK Backups\` |
| Debloat profiles | `Documents\FireForge\Profiles\` |
| Device reports | `Documents\FireForge\Reports\` |
| Screenshots | `Pictures\FireForge\` |
| Screen recordings | `Documents\FireForge\Recordings\` |

All of these can be opened from **Settings → Folders**.

---

## FAQ & troubleshooting

**"Device unauthorized" when connecting**
Look at the TV — it's asking you to allow debugging. Tick *Always allow from this computer* and press OK, then connect again.

**Can't connect at all**
Check the IP address, that ADB Debugging is on, and that the PC and TV are on the same network (not a guest network). Restarting the Fire TV usually clears an "offline" state.

**An app keeps coming back after an Amazon update**
Turn on the **Fire OS Update Shield**, and use **Scheduled Maintenance** on the Extra Tools page — it re-disables anything that comes back.

**Fire OS refused to disable an app**
Newer firmware protects some packages. FireForge offers to remove them for the current user instead (reversible). On a rooted device, **Root Tools** can disable them.

**Volume or power buttons on the remote page don't work**
They need HDMI-CEC switched on in your TV's settings.

**FireForge showed "Something went wrong"**
Press **Copy Error Details** in that window and paste it into a [new issue](https://github.com/FireForgeOffical/FireForge-Command-Center/issues/new). You can also copy diagnostics any time from **Settings → Updates**.

**I want to undo something FireForge did**
Open **Changes & History → History**, select the change (or any change from the same preset) and press **Undo Selected** or **Undo Whole Operation**.

**Windows SmartScreen warning**
New apps show this until they've built up a download history. Click **More info → Run anyway**. Only copies from this repository's Releases page are official.

---

## Privacy

FireForge has no accounts, telemetry, analytics or advertising. It only connects to:

- **your Fire TV**, over ADB on your local network or USB
- **GitHub**, to check for new FireForge versions and updated debloat definitions (both can be turned off in **Settings → Updates**)
- **an app's official website or GitHub page**, when you choose to install that app from the App Store
- **Google's public favicon service**, to fetch App Store icons, which are then kept on your PC

Your settings, snapshots, backups and logs stay on your PC.

---

## Licence

FireForge Command Center is free to download and use. Copyright © 2026 FireForge, all rights reserved. Please share a link to this page rather than re-uploading FireForge elsewhere, so everyone gets the genuine, up-to-date version.

FireForge includes Google's ADB Platform Tools, which are licensed separately by Google.

---

## Disclaimer

FireForge changes settings and app states on your device. It's provided as-is, without warranty — you use it at your own risk. Rooting, unlocking or flashing a device may void its warranty and can make it unusable. Always take a snapshot before making large changes.
