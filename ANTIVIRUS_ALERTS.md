# Antivirus Alerts & False Positives Explained

When you download and run the **GeForce NOW Discord Rich Presence** application, your antivirus software (such as Windows Defender) might flag the executable file (`Discord GFN.exe`) as potentially malicious. You might see alerts like "Trojan," "Malware-gen," "Wacapew," or similar warnings.

**Please be assured: These are almost certainly FALSE POSITIVES.** This application is safe to use.

### Why Do These Alerts Happen?

This is a very common occurrence for small, custom-built applications. Here's why:

1.  **Packaging Method:** The application is compiled into an executable using a method that antivirus programs often view with suspicion due to its unusual structure compared to traditional software.
2.  **Lack of Digital Signature:** The executable is not digitally signed by a recognized software publisher. Antiviruses often flag unsigned software as potentially risky simply because its origin isn't officially verified.
3.  **Heuristic Detection:** Antivirus software uses "heuristics" (behavior-based analysis) to detect new or unknown threats. Our application performs legitimate actions that can sometimes resemble suspicious behavior:
    * **Network Requests:** It connects to Steam servers to fetch game information and images.
    * **File Modifications:** It creates and modifies configuration files (`.json`) and downloads images (`.png`) in specific folders.
    * **System Tray & Startup Integration:** The application runs in the system tray and offers an option to start with Windows. These are legitimate features but can be flagged if an antivirus's heuristics are very aggressive.
4.  **Generic Flags:** The alerts you see (e.g., `Malware-gen`, `Wacapew`, `Sabsik`) are often generic detections, meaning the antivirus doesn't recognize a specific known virus but rather a pattern that *might* indicate malware.

### What Does This Mean for You?

The application is designed solely to enhance your Discord experience with GeForce NOW and contains no malicious intent. You are safe to use it.

### How to Allow the Application (Whitelist)

If your antivirus blocks the application or deletes its files, you will need to add an exception (whitelist) for the application's folder or the `Discord GFN.exe` executable. Here are instructions for **Windows Defender**, the most common built-in antivirus on Windows. Other antivirus programs will have similar steps.

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
        * Browse to the folder where you extracted the `GeForceNOW-Discord-Rich-Presence` application from the downloaded ZIP file (e.g., `C:\Users\YourUser\Documents\GeForceNOW-Discord-Rich-Presence`).
        * Select the entire main application folder and click **"Select Folder"**.
    * Alternatively, you can select **"File"** and add the executable individually:
        * `Discord GFN.exe`

6.  **Confirm the Exclusion:**
    * Confirm any prompts from User Account Control (UAC).
    * The folder/file will now appear in your exclusion list.

#### After Adding the Exclusion:

* If your antivirus quarantined or deleted the files, you may need to **restore them from quarantine** within your antivirus software.
* Once restored and excluded, you should be able to run `Discord GFN.exe` without further alerts.

If you are using a different antivirus program (e.g., Avast, AVG, McAfee, Norton), please consult its specific documentation for how to add exclusions or whitelist programs. The general principle remains the same.