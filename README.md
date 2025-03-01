# CLocker
> SharpCry-based ransomware with full file tree encryption and thread handling system.

## Screenshots
<img src="screenshot.png">
<img src="screenshot2.png">

# Disclaimer
> This software is intended ***exclusively for educational purposes and ethical cybersecurity research***. It is designed to help users understand potential vulnerabilities in systems so they can improve their security.
>
> By using this software, you agree to use it in compliance with all applicable laws and regulations. Unauthorized use, distribution, or deployment of this software against any system without the explicit permission of the system owner is strictly prohibited and may result in criminal and civil penalties.
>
> The creator(s) of this software assume no liability and are not responsible for any misuse or damages arising from the use of this software. Always obtain proper authorization before testing or analyzing systems using this software.

# Warning
> Be sure to read the license before using the project.
> **Because of the heavy use of Thread for encrypting files, we notify you in advance that the amount of files, regardless of file encryption, can cause critical damage to the CPU.**

# Purposes
> This project is a **Proof of Concept (PoC) malware designed to evaluate <ins>the ability of ransomware detection of anti-virus software</ins>** and assess their effectiveness in responding to and minimizing the impact of already executed malicious code.
> **<del>(No malicious actions are included in the source code.)</del>**

# Usage
> ## Execution
> **You must run server.py on the same server or it will not be activated.**<br>
> CLocker.exe --debug &:: DEBUG MODE: PRINTS ALL INFORMATION<br>
> CLocker.exe --force &:: ACTION MODE: ENCRYPT ALL FILES<br>
> **CLocker.exe --sandbox --force &:: ADVANCED DEBUG MODE: SET CUSTOM TARGET PATH**<br>
> Virtual machine detection and AES DLL hooking detection are disabled while running on sandbox mode.

> ## Configuration
```CSharp
public static string __KILL_SWITCH = "KILL_SWITCH_SERVER"; // i.e. http://localhost:8080/
```
> 
> **The kill switch will be automatically activate if the program cannot "access" to the link. This means if your kill switch server is NOT active, it will shutdown.**
