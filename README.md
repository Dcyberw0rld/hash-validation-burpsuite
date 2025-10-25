# 🔐 Validating File Integrity Using PowerShell (Burp Suite Example)

This project demonstrates how to verify the integrity and authenticity of a downloaded file using PowerShell’s built-in `Get-FileHash` command.  
In this example, I validated the **SHA-256 checksum** of the **Burp Suite Community Edition 2025.9.5 (Windows x64)** installer against the official checksum published by PortSwigger.

---

## 🧠 Learning Objectives

- Understand why file integrity validation is essential in cybersecurity  
- Learn how to compute and compare hash values using PowerShell  
- Apply real-world best practices for verifying software authenticity  

---

## ⚙️ Steps Performed

### 1. Downloaded Burp Suite
Official source:  
👉 [https://portswigger.net/burp/releases](https://portswigger.net/burp/releases)

### 2. Retrieved Official Checksum
From PortSwigger’s website:

SHA256: 89b64064dfaa8859dcb19ee472e505563270ffb0091b35c614eef8ebda78508

### 3. Opened PowerShell and Navigated to the Downloads Folder
```powershell
cd downloads

4. Generated Local File Hash
Get-FileHash .\burpsuite_community_windows-x64_v2025_9_5.exe -Algorithm SHA256

5. Compared Hash Values

Output:
Algorithm : SHA256  
Hash      : 89B64064DFAA8859DCB19EE472E505563270FFB0091B35C614EEF8EBDA78508  
Path      : C:\Users\Darryl\downloads\burpsuite_community_windows-x64_v2025_9_5.exe

✅ Result: The computed hash matched the official SHA-256 checksum exactly.
This confirms that the file has not been tampered with or corrupted during download.

🖼️ Evidence
🔹 PowerShell Verification


Screenshot of PowerShell showing the calculated SHA-256 hash using the Get-FileHash command.

🔹 Official Checksum Source


Official SHA-256 checksum displayed on PortSwigger’s website for the Burp Suite 2025.9.5 (Windows x64) release.

🔍 Why This Matters

Verifying file integrity is a fundamental cybersecurity practice that ensures:

🧩 Protection against tampered or malicious software

🧱 Defense against man-in-the-middle (MITM) attacks

✅ Validation of data integrity before installation

This aligns with the CIA Triad (Confidentiality, Integrity, Availability) — focusing on maintaining Integrity.

🧾 Technologies Used

PowerShell

SHA-256 Hashing Algorithm

Windows 11 (x64)
🧑‍💻 Author

Darryl Klu

🏁 Summary

This project highlights a real-world cybersecurity verification technique used by professionals to ensure software authenticity and integrity.
By validating file hashes, users can confidently install software knowing it has not been modified or compromised.


