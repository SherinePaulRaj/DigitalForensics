
# Digital Forensics & Incident Response (DFIR) Final Project

## Overview

This project involves a comprehensive forensic investigation of a hard drive image associated with a suspected malware writer. Using various digital forensic tools, we analyzed the disk image, uncovered encrypted files, decoded hidden messages, and identified potential malware activities.

## Tools Used

- **Autopsy**: Open-source digital forensics tool for disk image analysis, file examination, keyword searches, and more.
- **Wireshark**: Network protocol analyzer used for monitoring network traffic and capturing data packets.
- **VeraCrypt**: Encryption tool for decrypting encrypted volumes and extracting hidden data.

## Investigation Process

1. **Disk Image Analysis**: 
   - Imported the disk image into Autopsy to identify suspicious directories and files.
   - Found several artifacts, including executables (`obiwan.exe`, `obiwan2.exe`), encrypted files, and evidence of encryption software.

2. **Network Traffic Monitoring**:
   - Used Wireshark to capture network traffic during the execution of suspected malware.
   - Identified encrypted GET requests, which were decoded using Base64 to uncover critical information.

3. **Decryption and Data Extraction**:
   - Discovered an encrypted `.mp3` file that was mounted on VeraCrypt using a password derived from Wireshark analysis.
   - Decrypted the file, revealing additional malware components and important data such as "Death Star Plans."

## Key Findings

- **Suspicious Files**: Located several executables, encrypted files, and shortcuts leading to hidden malware components.
- **Encrypted Communications**: Decoded messages included:
  - "r2d2 is the key" (password for decryption)
  - Final transmissions: "We-have-the-blue-prints-to-the-Death-Star" and "We-will-defeat-Darth-Vader"
- **Data Artifacts**: Additional metadata, including Shell Bags and EXIF information, were found, pointing to specific user behaviors and encrypted files.

## Challenges Faced

- **Executable Identification**: Difficulty in distinguishing between the right executables due to misleading file names.
- **Password Decryption**: The need to decode Base64 encrypted URLs to determine the correct password for decryption.

## Recommendations

- **Optimize Firewall Rules**: Block unauthorized and repetitive requests to prevent malware communication.
- **Deploy Incident Response Systems**: Implement robust detection and periodic scans for early identification of threats.
- **Restrict System Privileges**: Limit software installations to administrators only to minimize risk.
- **Regular System Updates**: Ensure operating systems and applications are regularly updated to mitigate vulnerabilities.

## Conclusion

This investigation illustrates the critical role of comprehensive analysis in digital forensics, combining disk examination, network traffic monitoring, and encryption decryption to uncover hidden malware activities. The findings underscore the importance of proactive security measures and robust forensic practices.

## Author

- **Sherine Paul Raj** - Graduate Student, ENPM687 CY01
