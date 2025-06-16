## Antivirus Alerts & False Positives Explained

When you download and run the **GeForce NOW Discord Rich Presence** application, your antivirus software (such as Windows Defender) might flag some of the executable files (`Discord GFN.exe`, `Image Downloader.exe`, `Settings.exe`) as potentially malicious. You might see alerts like "Trojan," "Malware-gen," "Wacapew," or similar warnings.

**Please be assured: These are almost certainly FALSE POSITIVES.**

### Why Do These Alerts Happen?

This is a very common occurrence for small, custom-built applications, especially those created from Python scripts and packaged into standalone `.exe` files. Here's why:

1.  **PyInstaller Packaging:** The application is compiled into executables using a tool called PyInstaller. Antivirus programs are often suspicious of executables created this way because they bundle a Python interpreter and libraries, making their structure unusual compared to traditional software.
2.  **Lack of Digital Signature:** These executables are not digitally signed by a recognized software publisher. Antiviruses often flag unsigned software as potentially risky simply because its origin isn't officially verified.
3.  **Heuristic Detection:** Antivirus software uses "heuristics" (behavior-based analysis) to detect new or unknown threats. Our application performs legitimate actions that can sometimes resemble suspicious behavior:
    * **Network Requests:** It connects to Steam servers to fetch game information and images.
    * **File Modifications:** It creates and modifies configuration files (`.json`) and downloads images (`.png`) in specific folders.
    * **System Tray & Startup Integration:** The main application (`Discord GFN.exe`) runs in the system tray and offers an option to start with Windows. These are legitimate features but can be flagged if an antivirus's heuristics are very aggressive.
4.  **Generic Flags:** The alerts you see (e.g., `Malware-gen`, `Wacapew`, `Sabsik`) are often generic detections, meaning the antivirus doesn't recognize a specific known virus but rather a pattern that *might* indicate malware.

### What Does This Mean for You?

Since this project is open-source, you can inspect the Python source code (`main.py`, `image_downloader.py`, `config_editor.py`) to verify that there is no malicious intent. The application is designed solely to enhance your Discord experience with GeForce NOW.

### How to Allow the Application (Whitelist)

If your antivirus blocks the application or deletes its files, you will need to add an exception (whitelist) for the application's folder or specific executables. Here are instructions for **Windows Defender**, the most common built-in antivirus on Windows. Other antivirus programs will have similar steps.

#### For Windows Defender:

1.  **Open Windows Security:**
    * Click the **Start button**, type "Windows Security," and open the app.
    * Alternatively, find the **shield icon** in your system tray and double-click it.

2.  **Go to Virus & Threat Protection:**
    * In the Windows Security window, click on **"Virus & threat protection"** in the left-hand menu.

3.  **Manage Settings for Virus & Threat Protection:**
    * Under "Virus & threat protection settings," click on **"Manage settings."**

4.  **Add an Exclusion:**
    * Scroll down to the **"Exclusions"** section and click on **"Add or remove exclusions."**

5.  **Add Folder or File Exclusion:**
    * Click **"+ Add an exclusion"**.
    * Select **"Folder"**: This is the recommended option as it will whitelist all necessary files within the application's directory.
        * Browse to the folder where you extracted or cloned the `GeForceNOW-Discord-Rich-Presence` repository (e.g., `C:\Users\YourUser\Documents\GeForceNOW-Discord-Rich-Presence`).
        * Select the entire main application folder and click **"Select Folder"**.
    * Alternatively, you can select **"File"** and add each executable individually:
        * `Discord GFN.exe`
        * `Image Downloader.exe`
        * `Settings.exe`

6.  **Confirm the Exclusion:**
    * Confirm any prompts from User Account Control (UAC).
    * The folder/files will now appear in your exclusion list.

#### After Adding the Exclusion:

* If your antivirus quarantined or deleted the files, you may need to **restore them from quarantine** within your antivirus software.
* Once restored and excluded, you should be able to run `Discord GFN.exe` (or `Settings.exe`, `Image Downloader.exe`) without further alerts.

If you are using a different antivirus program (e.g., Avast, AVG, McAfee, Norton), please consult its specific documentation for how to add exclusions or whitelist programs. The general principle remains the same.
