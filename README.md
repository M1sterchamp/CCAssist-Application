# 🚛 CCAssist Core

![Version](https://img.shields.io/badge/version-1.1.11-yellow)
![Platform](https://img.shields.io/badge/platform-windows-blue)
![Electron](https://img.shields.io/badge/framework-Electron-FB3E44)

**CCAssist** is a dedicated automation tool designed for **Ghost Express CC** team members. It streamlines the preparation process for supervising events in Euro Truck Simulator 2 and American Truck Simulator by handling profile installation, DLC management, and in-game communication.

---

## ✨ Key Features

### 📂 Automated Profile Injection
No more manual unzipping or folder navigation.
- **Drag & Drop:** Simply drop a profile `.zip`, `.rar`, or `.7z` into the app.
- **Automatic Extraction:** Uses a bundled 7-Zip portable binary to handle all compression types.
- **Instant Activation:** Automatically moves files to your profiles directory.

### 🛠 Control Syncing
Maintain your muscle memory across different event profiles.
- Select your main profile from a dropdown.
- Sync your personal controls and keybinds to the newly imported event profile with one click.

### 📡 Auto Messenger (Event Broadcast)
Automate repetitive convoy control messages without leaving the game.
- **Custom Loop & Startup Delays:** Set how often messages send and give yourself time to alt-tab back into the game.
- **Global Hotkeys:** Start and stop the messenger using custom keybinds (default F9/F10), even while the app is minimized.
- **In-Game HUD:** A transparent overlay appears in the bottom-right of your screen to show countdowns and active status.

### 🛡 DLC Synchronization
Prevent "Missing DLC" crashes or accidental usage of restricted parts.
- Automatically detects dependencies from the profile.
- Updates TruckersMP launcher options to disable any DLCs not required by the specific event profile.
- Restores your original settings when the session is terminated.

---

## 🚀 Installation & Setup

1. **Download:** Grab the latest `CCAssist-Setup.exe` from the [Releases](https://github.com/M1sterchamp/CCAssist-Application/releases) page.
2. **First Run:** The application will attempt to auto-locate your TruckersMP and ETS2/ATS folders.
3. **Tutorial:** Follow the built-in interactive guide to ensure your paths are configured correctly.

---

## 📖 How to Use
1. **Authentication:** Open the app and click **LOG IN WITH DISCORD**. Your browser will open for verification. Once authorized, return to the app.
2. **Import:** Drag the event profile ZIP onto the Dashboard.
3. **Sync:** (Optional) Use the "Sync Controls" tool to copy your keybinds.
4. **Initialize:** Click **INITIALIZE TRUCKERSMP**. The app will configure your DLCs and launch the game.
4=5. **Messenger:** If you need to send convoy instructions:
    - Go to the **Auto Messenger** tab.
    - Input your message and set your delay.
    - Use **F9** to start and **F10** to stop. These can be configured to your liking in the panel.
6. **Cleanup:** Once the event is over, click **TERMINATE SESSION**. The app will delete the temporary profile and re-enable all your DLCs.

---

## 🛠 Technical Stack

- **Framework:** [Electron](https://www.electronjs.org/)
- **Automation:** [RobotJS](http://robotjs.io/) for simulating in-game keystrokes.
- **Updates:** [Electron-Updater](https://www.electron.build/auto-update) for mandatory system sync.
- **Utilities:** Bundled `7z.exe` for archive handling and `SII_decrypt.exe` for profile parsing.
- **Security:** Discord OAuth2 & API Key Header validation.

---

### 🔐 Discord Authentication & Whitelist
The application is secured by a real-time whitelist system handled by the **Ghost Express API**.
- **OAuth2 Handshake:** Secure login using official Discord credentials—no passwords stored.
- **Persistent Sessions:** Remembers your authorization status. You only need to log in once unless your access is revoked.
- **Live Verification:** Cross-references User IDs with a standalone SQLite database to prevent unauthorized access.

---

### 👑 Admin Management Hub
A high-level interface for team leads to manage system access.
- **Personnel List:** A full-width, searchable list of every authorized team member.
- **Access Control:** Instantly grant access to new members or revoke permissions with a single click.
- **Search & Filter:** Real-time filtering by Discord name or User ID for quick team audits.

---

## ⚠️ Requirements

- **OS:** Windows 10/11 (64-bit)
- **Game:** Euro Truck Simulator 2 or American Truck Simulator.
- **Permissions:** The app requires read/write access to your `Documents` and `AppData` folders to manage profiles and TruckersMP configs.
- **Authorisation:** The app requires authorisation through your Discord ID to allow you access into the application. The only data stored is your Discord ID. Which upon removal from the team, also gets deleted.

---

## 👨💻 Developed By

**Misterchamp**
*Created specifically for Ghost Express CC.*

---

## 📝 License
This project is proprietary and intended for use by authorized Ghost Express CC staff only. Use of the Auto Messenger for spamming in public TruckersMP servers is strictly against their rules and terms of service, and i, the developer of this software, nor Ghost Express will be held liable for any miss-use of the system. **Use responsibly.**

---
