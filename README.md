# ![DGFN](https://github.com/user-attachments/assets/42baa971-2f13-47ad-8274-5dfa4825f704)  GeForce NOW Discord Rich Presence

This application enhances your Discord experience by updating your Discord status with the game you're currently playing on **GeForce NOW**. It runs silently in your system tray, intelligently detecting and displaying the game's title, **cover art** on your Discord profile.

![Captura de pantalla 2025-06-14 213032](https://github.com/user-attachments/assets/3b04ce49-5453-45b5-a092-c3da90ef9396)
![Captura de pantalla 2025-06-14 213105](https://github.com/user-attachments/assets/8360f864-2f3b-45ce-a43d-e09d1970d58e)

## ✨ Features

* **Automatic Game Detection:** Seamlessly identifies the game you're playing on GFN.
* **Rich Presence Integration:** Displays game name, images, and playtime on Discord.
* **Steam Store Integration:** Fetches accurate game details and images from Steam for richer presence.
* **Automatic Status Clearing:** Resets Discord status when GFN inactive.
* **Customizable Settings:** Easily configure your Discord Application ID and other options via the application's user interface.
* **Built-in Image Downloader:** Download game images directly via the application for your Rich Presence assets.

---

## ⚠️ Important: Antivirus Alerts & False Positives

When you run `Discord GFN.exe`, your antivirus software (like Windows Defender) may flag it as potentially malicious. **Please be assured: This is a FALSE POSITIVE.** The application is safe to use.

For a detailed explanation of why these alerts occur and **how to allow the application in your antivirus**, please refer to the guide:
[Antivirus Alerts Troubleshooting Guide](ANTIVIRUS_ALERTS.md)

---

## 🚀 Setup and Installation

1.  **Download & Extract:**
    * Download the latest release `.zip` from the [Releases page](https://github.com/luisbrn/GeForce-NOW-Rich-Presence/releases) and extract its contents.

2.  **Deactivate Native Rich Presence:**
    * In NVIDIA GeForce NOW settings, disable the built-in "Discord Rich Presence" to prevent conflicts.

3.  **Create Discord Application:**
    * Go to the [Discord Developer Portal](https://discord.com/developers/applications/) and create a **New Application** (e.g., `GeForce NOW`).
    * Copy its **APPLICATION ID** from the "General Information" page.
    * **Upload a Default Image for Rich Presence:**
        * Discord Rich Presence requires at least one image asset to be uploaded to your application. This serves as a default or fallback image if specific game art isn't found.
        * Navigate to **"Rich Presence"** then **"Art Assets"** in the left-hand menu.
        * Upload the `default.png` file (found inside the application's folder after extracting the release `.zip`) and name the asset `default`. This ensures your presence always has a visual component.

4.  **Configure & Run:**
    * Double-click `Discord GFN.exe` to start the application. It will appear as an icon in your system tray.
    * **Left-click** the tray icon to open the **Manager Window**.
    * Go to the **"Settings"** tab, paste your **Application ID**, and click **"Save Config"**. The Rich Presence will restart to apply the new ID.

5.  **Using the Image Downloader:**
    * As you play games, the application caches their details.
    * To get high-quality images for your Rich Presence, open the Manager Window (via the tray icon) and go to the **"Image Downloader"** tab.
    * Click **"Start Image Download"**. The tool will automatically find your cached games and download their official art from Steam.
    * You will then need to upload these newly downloaded images from the `downloaded_capsules` folder to your Discord Developer Portal's "Art Assets" page.

6.  **Run at Windows Startup (Recommended):**
    * In the application's "Settings" tab (via the Manager Window), check the box for **"Run automatically when Windows starts"**.

---

## 🙏 Support

If you find this project useful, please consider supporting its development. You can find options on my "Buy Me A Coffee" page.
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/luisbrn)

## 📄 License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License.