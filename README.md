## GeForce NOW Discord Rich Presence v2.0
![DGFN_tray](https://github.com/user-attachments/assets/25b5b049-7340-4312-b7bc-f0971847c358)


This application updates your Discord status with the game you're currently playing on GeForce NOW. It runs in the background and clears your status when you stop playing or close GeForce NOW.

### Features

* Automatic game detection and Discord Rich Presence updates.
* Fetches game details and icons from Steam Store.
* **New:** Supports Russian, German, and Spanish game titles for detection.
* Clears Discord status when inactive.
* **New:** Prevents multiple script instances.
* **New:** System tray icon for easy management and exit.
* **New:** Option to auto-start with Windows via tray icon.
* **New:** Customizable tray icon (`DGFN_tray.png`).
* **New:** Improved image fitting; Discord uploads now expect PNG format.

### Requirements

* Windows OS
* Discord account
* GeForce NOW application

## Screenshots
![Captura de pantalla 2025-06-14 213124](https://github.com/user-attachments/assets/c5b9d5be-affd-49fb-8d7b-098b46cfea99)
![Captura de pantalla 2025-06-14 213032](https://github.com/user-attachments/assets/98350c6f-1623-42e8-8614-e57b457b3238)
![Captura de pantalla 2025-06-14 213105](https://github.com/user-attachments/assets/d38606d6-34c0-4999-91de-4cb426d9a966)


### Installation & Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/luisbrn/GeForceNOW-Discord-Rich-Presence.git](https://github.com/luisbrn/GeForceNOW-Discord-Rich-Presence.git)
    ```
    (Or download and extract the ZIP.)

2.  **Discord Application Setup:**
    * **Deactivate Rich Presence in GeForce NOW.**
    * Go to [Discord Developer Portal](https://discord.com/developers/applications/), create a **New Application**, and **copy its Application ID**.
    * Navigate to "Rich Presence" -> "Art Assets" in your Discord app. Upload a small placeholder PNG image (e.g., named `default`) and "Save Changes".

3.  **Configure Application ID:**
    * Double-click `Settings.exe` in the repository folder.
    * Paste your Discord **Application ID** into the "Discord Client ID" field.
    * (Optional) Set "Refresh Interval" (e.g., `2` seconds).
    * Click "Save Config".

4.  **Download Game Images & Upload to Discord:**
    * Launch a few games on GeForce NOW while `Discord GFN.exe` is running to populate game data.
    * Close `Discord GFN.exe`. Then, double-click `Image Downloader.exe`. This will download and process game images to the `downloaded_capsules` folder.
    * Go back to Discord Developer Portal -> "Rich Presence" -> "Art Assets". **Upload the PNG images** from `downloaded_capsules` (e.g., `1091500.png`) using their respective AppIDs as names. Click "Save Changes".

5.  **Run the Program:**
    * Double-click `Discord GFN.exe`. It will run in the system tray.
    * **To auto-start with Windows:** Right-click the tray icon and select "Start at Windows Startup".

### Troubleshooting / Antivirus Alerts

If your antivirus software flags the application files (`Discord GFN.exe`, `Image Downloader.exe`, `Settings.exe`) as malicious, please read our detailed explanation and instructions on how to whitelist the application here: [ANTIVIRUS_ALERTS.md](https://github.com/user-attachments/files/20765330/ANTIVIRUS_ALERTS.md)
. These are likely false positives due to how the application is packaged and operates.

Enjoy your new Rich Presence!

**Notes:**
* Logs are created in the `logs` folder.
* You can customize the tray icon by replacing `assets/DGFN_tray.png`.

## License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

**Important Notes on Usage:**
* You are free to share and adapt this software for personal, non-commercial use.
* You must provide appropriate attribution to the original author (luisbrn).
* Commercial use of this software is not permitted under this license.

If you like it and feel is useful for you, support me if possible:

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/luisbrn)
