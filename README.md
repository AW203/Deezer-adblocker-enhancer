# 🎵 Deezer Enhancer

Deezer Enhancer is an advanced, automated patcher for the Deezer Desktop App (Windows).  
It unlocks the full potential of the client by removing distractions, enforcing a true dark theme, and improving privacy—all with zero latency.

[Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)  
[Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge)  
[License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## ✨ Features

### 🚫 Ad Blocking (Universal)
- Audio Ads: Blocks audio interruptions via network interception and skip logic.
- Sidebar: Removes the "Subscribe" / "Upgrade" cards intelligently without breaking navigation.
- Dropdown: Removes promo banners from the user profile menu.
- Cache Cleaning: Automatically wipes Deezer's cache before patching to prevent old cached ads from reappearing.

### 🎨 True AMOLED Theme
- Deep Black: Forces a #000000 background across the entire app (Sidebar, Player, Header, Main Content).
- Zero Latence: Uses injected CSS for instant styling—no white flashes on startup.
- Consistency: A JavaScript watchdog ensures no element remains gray.
- Styled Menus: Custom dark borders and shadows for dropdowns and popups.

### 🛡️ Privacy & Performance
- Privacy Shield: Blocks requests to Sentry.io, Google Analytics, and Deezer logging endpoints.
- Performance Mode: Automatically disables Hardware Acceleration to reduce GPU usage and improve battery life on laptops.

### 🌍 International & Custom
- Universal Support: Works with English, French, German, Spanish, and Portuguese interfaces.
- Premium Branding: Replaces "Free" badges and window titles with "Deezer Premium".
- Custom Links: Adds direct shortcuts to community resources in the user settings menu.

---

## 📋 Prerequisites

### Deezer Desktop App
- Must be installed from the official website.
- ❌ NOT compatible with the Microsoft Store version.

### Node.js
- Required to repack the application files (asar).
- Download Node.js Here (LTS version recommended).

---

## 🚀 Installation

1. Download the latest `patch.ps1` file from the Releases page.
2. Right-click the file.
3. Select **"Run with PowerShell"**.
4. Wait for the process to finish (approx. 15–30 seconds).

The script will automatically:
- stop Deezer
- clean the cache
- backup original files
- apply the patch
- restart the app

---

## 🛠️ How It Works

This tool modifies `app.asar`, the core archive of the Electron application.

### Main Process Hooks
- Intercepts `session.defaultSession.webRequest` to block ad servers  
  (Google IMA, SmartAdServer, DoubleClick).

### Renderer Injection
- Injects CSS and a highly optimized MutationObserver (1ms trigger)  
  to modify DOM elements instantly.

### Protection
- Prevents the app from overwriting changes during runtime.

---

## 🔙 Uninstall / Restore

A backup of the original file is automatically created.

To restore Deezer:
1. Navigate to  
   `%LOCALAPPDATA%\Programs\deezer-desktop\resources\`
2. Delete the patched `app.asar`.
3. Rename `app.asar.original` to `app.asar`.
4. Restart Deezer.

---

## ⚠️ Disclaimer

This software is for educational purposes only.  
The author is not responsible for any account suspensions or issues resulting from the use of this tool.  
If you enjoy Deezer and want to support the artists, please consider purchasing a legitimate subscription.

---

## ❤️ Credits

**@htdf** — Lead Developer & Research
