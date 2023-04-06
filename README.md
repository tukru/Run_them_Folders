Title:         Multi-purpose Penetration Testing Payload

Author: TUKRU  
                              
Version:       1.0
Date:          2023-03-20
Description:   This payload performs multiple penetration testing tasks on a target Windows machine, including capturing saved wireless keys, taking screenshots, capturing images from the webcam, installing and running Nmap, capturing the SAM registry hive, DNS poisoning, and collecting IP configuration details. This README provides a detailed overview of the payload's functionalities and usage instructions.

Disclaimer:    Using this payload for unauthorized access, data theft, or any malicious activity is illegal and unethical. The information provided here is for educational purposes only and should not be used for malicious purposes. Always obtain explicit permission from the owner of the target system before attempting to use any penetration testing tools or techniques.

Payload overview:
-----------------
1. Retrieve saved wireless keys.
2. Take a screenshot.
3. Capture an image using the camera.
4. Install Nmap.
5. Run an Nmap scan on a specified IP range.
6. Capture the SAM registry hive.
7. Modify the HOSTS file for DNS poisoning.
8. Collect IP configuration details using the `ipconfig /all` command.

Usage instructions:
-------------------
1. Copy the DuckyScript payload to a text file named "payload.txt".
2. If you have not already done so, add the PhotoBooth class definition to the PowerShell window before running the DuckyScript payload.
3. Convert the "payload.txt" file to a binary payload using the DuckEncoder.
4. Copy the binary payload to the root of the Rubber Ducky USB flash drive.
5. Insert the Rubber Ducky into the target Windows machine.
6. The payload will execute automatically, performing the tasks mentioned in the Payload overview section.

Output:
-------
The following files will be saved on the target machine's Desktop:
- savedwirelesskeys.txt: Contains the retrieved wireless keys.
- screencapture.png: The captured screenshot.
- webcam.jpg: The captured image from the webcam.
- nmap_scan_results.txt: Results of the Nmap scan.
- sam: A copy of the SAM registry hive.
- ipconfig_all.txt: Output of the `ipconfig /all` command.

The HOSTS file located at "C:\Windows\System32\drivers\etc\hosts" will be modified to add a DNS poisoning entry.

Notes:
------
- This payload is designed for Windows systems. Some commands may need to be adjusted to work on macOS or Linux systems.
- Depending on the target machine's security settings, some tasks may be blocked by security software or require administrative privileges to execute.
