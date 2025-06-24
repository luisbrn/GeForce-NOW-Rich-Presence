<p align="center">
  <img src="https://github.com/user-attachments/assets/42baa971-2f13-47ad-8274-5dfa4825f704" alt="DGFN Logo">
  <h1 align="center">GeForce NOW Discord Rich Presence</h1>
</p>

<p align="center">
  <a href="https://github.com/luisbrn/GeForce-NOW-Rich-Presence/releases"><img src="https://img.shields.io/github/v/release/luisbrn/GeForce-NOW-Rich-Presence?style=for-the-badge" alt="Latest Release"></a>
  <a href="https://creativecommons.org/licenses/by-nc/4.0/"><img src="https://img.shields.io/badge/license-CC_BY--NC_4.0-blue?style=for-the-badge" alt="License"></a>
  <a href="https://www.buymeacoffee.com/luisbrn"><img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-orange?style=for-the-badge&logo=buymeacoffee" alt="Buy Me A Coffee"></a>
</p>

This application enhances your Discord experience by updating your status with the game you're currently playing on **GeForce NOW**. It runs silently in your system tray, intelligently detecting and displaying the game's title and **cover art** on your Discord profile.

---

### **Table of Contents**
- [✨ Features](#-features)
- [📸 Screenshots](#-screenshots)
- [🛠️ Prerequisites](#️-prerequisites)
- [🚀 Setup and Installation](#-setup-and-installation)
- [💡 Usage](#-usage)
- [🤔 Troubleshooting & FAQ](#-troubleshooting--faq)
- [🙏 Support](#-support)
- [📄 License](#-license)

---

## ✨ Features

* **Automatic Game Detection:** Seamlessly identifies the game you're playing on GFN.
* **Rich Presence Integration:** Displays game name, cover art, and playtime on Discord.
* **Steam Store Integration:** Fetches accurate game details from Steam for a richer presence.
* **Automatic Status Clearing:** Resets your Discord status when GFN becomes inactive.
* **Customizable Settings:** Easily configure your Discord Application ID via the UI.
* **Built-in Image Downloader:** Download game cover art directly through the application.
* **Run at Startup:** Optional setting to launch the app automatically with Windows.

## 📸 Screenshots

<table>
  <tr>
    <td align="center"><b>Discord Profile View</b></td>
    <td align="center"><b>Discord Profile View</b></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/3b04ce49-5453-45b5-a092-c3da90ef9396" alt="Discord Profile Screenshot"></td>
    <td><img src="https://github.com/user-attachments/assets/8360f864-2f3b-45ce-a43d-e09d1970d58e" alt="Discord Detailed View Screenshot"></td>
  </tr>
</table>

## 🛠️ Prerequisites

Before you begin, ensure you have the following:
* A Windows Operating System.
* An active [NVIDIA GeForce NOW](https://www.nvidia.com/en-us/geforce-now/) account.
* A [Discord](https://discord.com/) account and the desktop client installed.

## 🚀 Setup and Installation

1.  **Download & Extract**
    * Download the latest `.zip` file from the [**Releases page**](https://github.com/luisbrn/GeForce-NOW-Rich-Presence/releases).
    * Extract all the contents to a permanent folder on your computer.

2.  **Disable Native Rich Presence**
    * In the NVIDIA GeForce NOW app, go to `Settings`.
    * Turn **off** the built-in "Discord Rich Presence" to prevent conflicts.

3.  **Create a Discord Application**
    * Go to the [**Discord Developer Portal**](https://discord.com/developers/applications/) and click **"New Application"**.
    * Give it a name (e.g., `GeForce NOW`) and create it.
    * On the **"General Information"** page, copy the **`APPLICATION ID`**. You will need this later.

4.  **Configure & Run the App**
    * Double-click `Discord GFN.exe` to start the application. It will appear as an icon in your system tray.
    * **Left-click** the tray icon to open the **Manager Window**.
    * Go to the **"Settings"** tab, paste your **Application ID**, and click **"Save Config"**. The Rich Presence will restart to apply the change.

5.  **Upload Rich Presence Images**
    * Rich Presence requires at least one default image in your Discord Application.
    * In the Discord Developer Portal, navigate to **"Rich Presence"** > **"Art Assets"**.
    * Upload the `default.png` file (from the folder you extracted) and name the asset `default`.
    * To add more game images, see the [Usage](#-usage) section below.

6.  **Run at Startup (Recommended)**
    * In the app's Manager Window, go to **"Settings"**.
    * Check the box for **"Run automatically when Windows starts"** and save.

## 💡 Usage

* **Running in the Background:** The application runs silently in the system tray. As long as it's running, it will automatically detect games you play on GeForce NOW.
* **Manager Window:** **Left-click** the tray icon at any time to open the Manager Window. Here you can access settings and the image downloader.
* **Adding New Game Images:**
    1.  After playing new games, open the Manager Window and go to the **"Image Downloader"** tab.
    2.  Click **"Start Image Download"**. The tool will download official art for your recently played games into the `downloaded_capsules` folder.
    3.  Upload the downloaded images to your Discord Application's **"Art Assets"** section. **The name of the asset must match the game's App ID** (the image filename is already correctly named for this).

## 🤔 Troubleshooting & FAQ

> [!IMPORTANT]
> ### **Antivirus Alerts (False Positives)**
> When you run `Discord GFN.exe`, your antivirus (like Windows Defender) may flag it as malicious. **This is a false positive.** The application is safe to use.
> 
> Unsigned applications written in languages like Python are often flagged by heuristics. For a detailed explanation and a guide on **how to allow the app**, please read:
> **[Antivirus Alerts Troubleshooting Guide](ANTIVIRUS_ALERTS.md)**

## 🙏 Support

If you find this project useful, please consider supporting its development!

<a href="https://www.buymeacoffee.com/luisbrn" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;" ></a>

## 📄 License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).
