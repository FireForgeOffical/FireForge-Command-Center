FireForge Command Center

A free Windows toolkit to debloat, speed up, protect and control Amazon Fire TV and Fire TV Stick devices — no root needed.

FireForge connects to your Fire TV over your home Wi-Fi using ADB (Android Debug Bridge) and gives you one dark, modern dashboard to switch off Amazon’s bloat and tracking, block forced updates, install apps, control the TV from your PC and keep everything the way you set it up.

Every change is reversible. FireForge never deletes Amazon’s system files.

FireForge is free software and is not affiliated with, endorsed by or sponsored by Amazon. “Amazon”, “Fire TV” and “Fire TV Stick” are trademarks of Amazon.com, Inc. or its affiliates.

Contents
Highlights
Download & install
Getting connected
Features in detail
Safety & undo
Supported devices
Where FireForge keeps files
FAQ & troubleshooting
Building from source
Disclaimer

Highlights

🧹 Debloat – switch off Amazon services one by one or with one-click presets, from Safe to Extreme, each with a risk rating

⚡ Optimize – faster menus, background apps stopped, caches cleared and tracking switched off in one click

🛡️ Shields & DNS – block forced Fire OS updates, encrypted ad-blocking DNS, ad-tracking and Wi-Fi-scan controls

📦 App Store – 28 popular TV apps installed straight from their official sources, with update checks, plus drag-and-drop APK sideloading

🎮 Remote Control – a live view of the TV screen, a full remote, typing from your PC and screenshots; your keyboard becomes the remote

🔁 Automation – apply a setup to several Fire TVs at once, keep each one tidy on a timer, and export a shareable device report

💾 Backup & Restore – snapshots of which apps are off, and APK backups before anything is removed

🩺 Health Check – a score with one-click fixes, plus live CPU, memory, storage and temperature

🔓 Root & Recovery – bootloader/root status, a pre-root checklist and the right guide for your exact model

🖥️ Self-contained – one installer, no .NET or ADB install needed

Download & install
Go to the Releases page.
Download either:
FireForge-Setup-x.y.z.exe – installer with Start-menu shortcut and uninstaller, or
FireForge-x.y.z-portable-win-x64.zip – unzip anywhere and run FireForge.exe.
Run it. If Windows SmartScreen shows “Windows protected your PC”, click More info → Run anyway (this appears for new apps that aren’t code-signed yet).
Requirements: Windows 10 or 11 (64-bit), and the PC and Fire TV on the same network. Everything else, including ADB, is built in.

FireForge checks GitHub for new versions once a day (you can turn this off in Settings) and offers to download the installer when one is available.

Getting connected
On the Fire TV, open Settings → My Fire TV → About and click your device name 7 times until it says you’re a developer.
Go back to My Fire TV → Developer Options and switch ADB Debugging on.
Find the TV’s IP address under Settings → My Fire TV → About → Network (for example 192.168.0.18).
In FireForge, type the IP in the top bar and press Connect — or press Scan to find Fire TVs on your network.
The first time, the TV asks “Allow USB debugging?” — tick Always allow from this computer and press OK with the remote.
FireForge remembers each device you connect to (see Devices ▾ in the top bar), reconnects to the last one on start-up, and reconnects automatically if the connection drops.

Features in detail
The sidebar is split into Menu, Device and Help. Pages that do similar jobs share one sidebar entry with tabs along the top.

📊 Dashboard
Overview tab

Model, Fire OS and Android version, CPU, display, storage, memory, network and uptime
A screenshot of what’s on the TV right now
Power controls: reboot, reboot to recovery or bootloader, shut down, force-stop all apps
Device Report button (see Automation)
Health Check tab

A health score with a list of issues and one-click fixes (or Fix All)
Live CPU, memory, storage and temperature tiles
The apps using the most memory right now
🧹 Debloat
Presets tab

One-click bundles of changes graded Safe, Recommended, Aggressive and Extreme
Search and filter by severity; restore any preset just as easily
Apply to Several Devices jumps to Batch Mode on the Automation page
All Services tab

Every Amazon service FireForge knows about, grouped into categories (telemetry, ads, OTA updates, Alexa, built-in Amazon apps, screensavers, kids’ controls and core OS services), each with a description and risk rating
Filter by risk, search by name or package, tick what you want, then Disable, Remove or Restore
Export / Import profiles (.fireforge.json) to reuse your picks on another stick or share them
If Fire OS refuses to disable something, FireForge offers to remove it for the current user instead (backing the APK up first), and remembers which packages are protected so you aren’t asked again
⚡ Optimize
One-click tune-ups that work on every model:

Balanced Boost – 0.5× animations, stops background apps, clears app caches
Maximum Performance – animations off, telemetry and ad services disabled, ad tracking limited, background Wi-Fi scans off
Revert to Stock – puts everything back
A live Current State card shows how the device is tuned right now
📱 App Manager
Every installed app with status, type (system or user), size and a risk rating
Filter, search and sort by any column
Disable, Enable / Restore, Remove (with an automatic APK backup) and Clear Data — one app or many at once
A storage summary showing how much space apps use
🛍️ App Store
App Store tab — popular apps, always from the official source, never a mirror site. Filter by category, search, or show only installed apps.

MD
CSV
Export all to Excel
↔ Expand
Full
Developer’s GitHub releases	SmartTube, Jellyfin, Moonfin, Moonlight, Aerial Views, mpv, Just Player, TV Bro, LocalSend	Downloads the build that matches your stick’s processor, installs it, checks for updates and offers to open it
Amazon Appstore	Downloader, VLC, Netflix, YouTube, Disney+, Apple TV, Paramount+, Crunchyroll, Pluto TV, Tubi, Plex, Emby, Stremio, Spotify, X-plore File Manager, Send Files to TV, AirScreen, Analiti Speed Test	Opens the app’s Appstore page on the TV so you can install it with the remote
Developer’s website	Kodi	Opens the official download page
After installing Aerial Views, FireForge can set it as the Fire TV screensaver (normally only possible with ADB commands).

Sideload APKs tab

Drag APK files onto the page (or pick them) and install them all in one go
Failed installs stay in the list with the reason, ready to retry
🎮 Remote Control
Live view of the TV screen next to a full remote: d-pad, Back, Home, Menu, rewind / play-pause / fast-forward, volume, mute, sleep, wake and Settings
Type on the TV – send text to the selected box (much faster than the on-screen keyboard for passwords and URLs), plus Delete and Enter keys
Save Screenshot to your Pictures folder
Keyboard control – while this page is open, use the arrow keys, Enter, Backspace (Back), Home and Space (play/pause)
📁 File Transfer
Browse the Fire TV’s storage
Drag files from your PC to upload them, or download files back to the PC
Create folders and delete files
🛡️ Shields & DNS
Each card shows the current setting and lets you switch it on or off:

Fire OS Update Shield – stops Amazon pushing system updates that can undo debloating (and can be restored any time)
Encrypted Private DNS – AdGuard, Mullvad, Cloudflare, Quad9, Google or your own provider (for example NextDNS)
Interest-based ads, connectivity check pings and background Wi-Fi scanning
A shortcut to the TV’s own privacy settings (usage data and content recognition)
💾 Backup & Restore
Snapshots record exactly which apps are disabled or removed; restore one to roll the device back to that state
APK backups are saved to your PC automatically before any app is removed
🔁 Automation
Batch Mode – pick a preset or profile, Balanced Boost and/or the privacy shields, tick your saved Fire TVs, and FireForge applies it to each one in turn, then reconnects to the device you started on
Scheduled Maintenance – every 1–24 hours while FireForge is open: clears caches, stops background apps, puts shield settings back, and re-disables or re-removes apps that an Amazon update switched back on. It compares against a saved baseline for each device.
Device Report – a one-page HTML summary of a device (model, Fire OS, storage, memory, every disabled or removed app, and the state of each shield). Print it to PDF from your browser. Serial number, MAC address, IP and Wi-Fi name are left out so it’s safe to share.
🔓 Root & Recovery
FireForge never runs exploits, roots or flashes anything automatically — that’s model-specific and doing it blindly can brick a device. Instead it:

Detects the model and codename, Fire OS and Android version, security patch, bootloader lock state, root (Magisk) and SELinux
Shows a pre-root checklist: firmware noted, updates blocked, snapshot taken, fastboot available
Opens the right community guide for your exact model, and links to official firmware and the XDA forum
Reboots to recovery or the bootloader, and checks fastboot status (when fastboot.exe is in the adb folder)
Root Tools (rooted devices only): test root access, and disable apps Fire OS refused to switch off
Copy Info puts your device details on the clipboard, ready to paste when asking for help
🧰 Extra Tools
Launch or force-stop any installed app
Custom launcher – install a third-party home screen, try to make it the default, or go back to Amazon’s
TV shortcuts: Fire TV settings, network settings, developer options and restart the home screen
Interface animation speed, display resolution and screen density (DPI) overrides
🖥️ Terminal & Logs
Run your own ADB shell commands
See everything FireForge does, with timestamps
Read the Fire TV’s own live, colour-coded system log (logcat)
⚙️ Settings
Connection – reconnect on start-up, connection watchdog and how often it checks, default ADB port
Safety – APK backup before removing, confirm before reboot or shut-down, show the terms notice only once, forget the list of protected apps
Interface – remember window size, which page opens at start-up, refresh speeds for live stats, logs and the Remote Control view
Logging – timestamps, and saving the log to a file (one per day)
Updates – check on start-up, check now, un-skip versions, release notes
Folders – one-click access to every folder FireForge uses
Reset – forget saved devices, or reset all settings (devices, snapshots, profiles and backups are kept)
Safety & undo
Disabled apps stay on the device and come back with Restore on the Debloat, Presets or App Manager pages.
Removed apps are only removed for the current user — the original stays in the system partition, so Enable / Restore in App Manager brings it back. FireForge also saves the APK to your PC first.
Take a snapshot in Backup & Restore before trying Aggressive or Extreme presets.
If something goes badly wrong, a factory reset from the Fire TV’s settings returns it to stock.
Disabling some services can stop Amazon features working (for example recommendations, Alexa or the Appstore). Every item shows a risk rating, and the Safe and Recommended presets avoid anything that breaks normal use.

Supported devices
FireForge works with Fire TV devices running Fire OS 5, 6, 7 or 8 that have ADB Debugging in Developer Options, including:

Fire TV Stick (all generations), Fire TV Stick Lite, Fire TV Stick 4K, Fire TV Stick 4K Max, Fire TV Cube, Fire TV boxes and Fire TV Edition smart TVs.

Newer Fire TV devices running Vega OS (not Android-based) are not supported. Some packages are protected by Fire OS on newer firmware and can’t be disabled without root — FireForge tells you when that happens.

Where FireForge keeps files
MD
CSV
Export all to Excel
Full
Settings, saved devices, snapshots	%AppData%\FireForge\
Log files (if enabled)	%AppData%\FireForge\Logs\
APK backups	Documents\FireForge\APK Backups\
Debloat profiles	Documents\FireForge\Profiles\
Device reports	Documents\FireForge\Reports\
Screenshots	Pictures\FireForge\
All of these can be opened from Settings → Folders.

FAQ & troubleshooting
“Device unauthorized” when connecting
Look at the TV — it’s asking you to allow debugging. Tick Always allow from this computer and press OK, then connect again.

Can’t connect at all
Check the IP address, that ADB Debugging is on, and that the PC and TV are on the same network (not a guest network). Restarting the Fire TV usually clears an “offline” state.

An app keeps coming back after an Amazon update
Turn on the Fire OS Update Shield, and use Scheduled Maintenance on the Automation page — it re-disables anything that comes back.

Fire OS refused to disable an app
Newer firmware protects some packages. FireForge offers to remove them for the current user instead (reversible). On a rooted device, Root Tools can disable them.

Volume or power buttons on the remote page don’t work
They need HDMI-CEC switched on in your TV’s settings.

Windows SmartScreen warning
FireForge is new and not yet code-signed. Click More info → Run anyway.

Disclaimer
FireForge changes settings and app states on your device. It’s provided as-is, without warranty — you use it at your own risk. Rooting, unlocking or flashing a device may void its warranty and can make it unusable. Always take a snapshot before making large changes.
