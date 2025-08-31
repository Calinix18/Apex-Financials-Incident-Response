🛡️ Apex Financials – Cybersecurity Incident Response
<p align="center"> <img src="https://img.shields.io/badge/University-SUNY%20Albany-purple?style=for-the-badge&logo=grad" /> <img src="https://img.shields.io/badge/Spring-2025-blue?style=for-the-badge&logo=calendar" /> <img src="https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-green?style=for-the-badge&logo=open-source-initiative" /> </p>
📂 Repository Contents
File	Description
INC250306_Report_Part1.pdf	Technical report – Spear-phishing → ShadowCrypt ransomware incident
Part1_Assignment_Guidelines.pdf	Faculty-provided task description & scope
INC250422_Report_Part2.pdf	Technical report – Web server compromise & web shell backdoor
Part2_Assignment_Guidelines.pdf	Project resources: network diagram, asset roles, and scope
Part2_SourceLogs.pptx	Provided logs and attack hints
Part2_Readme_Clue.txt	Decoding clue / assignment identifier
Part2_Presentation.pdf	Final presentation with summary and takeaways
🔍 Incident 1 – ShadowCrypt Ransomware (INC250306)

🎯 Attack Vector: Spear-phishing email with malicious PDF

💻 Initial Target: WORKSTATION-01 (apexfinancial\analyst1)

⚡ Execution: Malicious macro → (T1204.002)

🔑 Credential Access: Brute-force + Pass-the-Hash (T1110, T1550.002)

🔄 Lateral Movement: WMI + PsExec

💣 Final Payload: ShadowCrypt ransomware on server 192.168.1.200

⏳ Persistence: Scheduled tasks (T1053.005)

IOCs:
📎 Q1 Performance Review.pdf
🌐 C2: 185.143.223.47
🛠️ Registry & scheduled task artifacts

🔎 Incident 2 – Web Server Compromise (INC250422)

🚪 Initial Entry: Brute-force /login.php

🐚 Exploitation: SQLi + Web shell upload (c99shell.php, eval-stdin.php)

🖥️ Commands: cmd=ls, cmd=whoami via PHP shell

📤 Exfiltration: >50GB data → 167.172.3.114

db_config.php, backup.tar.gz, .csv/.xls

Mapped MITRE ATT&CK:
🔑 T1110 – Brute Force
🐚 T1505.003 – Web Shell
⚙️ T1059.003 – PHP Execution
📡 T1041 – HTTP Data Exfiltration

🛠️ Tools & Frameworks
<p align="center"> <img src="https://img.shields.io/badge/Splunk-Log%20Correlation-orange?style=for-the-badge&logo=splunk" /> <img src="https://img.shields.io/badge/Wireshark-Packet%20Analysis-blue?style=for-the-badge&logo=wireshark" /> <img src="https://img.shields.io/badge/Security%20Onion-IDS/NSM-teal?style=for-the-badge&logo=security" /> <img src="https://img.shields.io/badge/PowerShell-Forensics-blue?style=for-the-badge&logo=powershell" /> <img src="https://img.shields.io/badge/Linux-CLI%20Analysis-black?style=for-the-badge&logo=linux" /> </p>
📑 Key Lessons

✔️ Email filtering & phishing awareness training
✔️ MFA & strong credential policies
✔️ WAF + input validation for web apps
✔️ Forensic readiness (log hashing, disk imaging)

👨‍💻 Contributors

Sriram R 🔵

Leela Pavan 🟢

Shalem Raju 🟠

SriVarsha A 🟡

Junaid M 🔴

Phanindhar Reddy K 🟤

📄 License

📝 Licensed under CC BY-NC-ND 4.0
