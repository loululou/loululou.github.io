---
title:  "Install Windows 11 on Mac"
layout: post
categories: 
  - notes
permalink: /notes/2025-01-05-installation-M2
last_modified_at: 2025-01-05
---

Just a note.. 

---

When installing Windows 11 on a Mac with an M chip, you might encounter an issue: no network access.  

At this screen, press `Shift + FN + F10` to open the command prompt.  
Then, type the command `OOBE\BYPASSNRO` and press Enter. The system will reboot.  

After the reboot, select the option "I don't have internet access" to proceed with the installation process.  

Then, after installation, you may still find no internet access.  

To fix this, install VMware Tools.  
- Double click "setup" to install VMware Tools.  
- After installation, the system will reboot again. Now, your internet connection should be working.  

#### Visual Studio 
- https://learn.microsoft.com/en-us/visualstudio/install/visual-studio-on-arm-devices?view=vs-2022  
- https://visualstudio.microsoft.com/vs/  

# Disable Microsoft Defender  
Steps to Disable Microsoft Defender  
1. Run `msconfig` as Administrator
- Go to the Boot tab.
- Enable Safe Boot by checking the box.
- Click OK and restart Windows.  

2. Run gpedit.msc, Navigate to:
- Computer Configuration → Administrative Templates → Windows Components → Microsoft Defender Antivirus.
- Locate Turn off Microsoft Defender Antivirus.  
Set it to Enabled and click OK.  

Reboot the system to apply all changes.
