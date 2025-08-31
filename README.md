# Apex-Financials-Incident-Response
Part 1: Spear-phishing &amp; ransomware attack report (INC250306)  Part 2: Web server compromise with c99shell backdoor (INC250422)

# 🛡️ Apex Financials – Incident Response Report (Part 1 & Part 2)

This repository documents two separate but high-impact cybersecurity incidents that occurred at Apex Financials. These incidents were investigated using industry-standard tools (Splunk, Wireshark, IDS, firewall analysis) and mapped to MITRE ATT&CK tactics.

---

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

Attack Vector: Spear-phishing email with malicious PDF

Initial Compromise: WORKSTATION-01 (user: apexfinancial\analyst1)

Execution: Malicious macro in PDF (T1204.002)

Credential Access: Brute-force + Pass-the-Hash (T1110, T1550.002)

Lateral Movement: WMI & PsExec

Impact: Deployment of ShadowCrypt ransomware on server 192.168.1.200

Persistence: Scheduled tasks created (T1053.005)

IOCs:

Malicious attachment: Q1 Performance Review.pdf

C2 Server: 185.143.223.47

Registry edits & scheduled task artifacts

Business Impact:
Operational downtime, risk of intellectual property theft, and financial record loss.

🔎 Incident 2 – Web Server Compromise (INC250422)

Initial Access: Brute-force login to /login.php

Exploitation:

SQL Injection

Web shell upload (c99shell.php, eval-stdin.php)

Command execution via PHP (cmd=ls, cmd=whoami)

Exfiltration: 50GB+ of sensitive data → 167.172.3.114

Stolen files: db_config.php, backup.tar.gz, multiple .csv/.xls datasets

Analyzed Logs:

Web access logs

IDS alerts

Firewall logs

Mapped MITRE Techniques:

T1110 – Brute Force

T1505.003 – Web Shell

T1059.003 – PHP Command Execution

T1041 – Data Exfiltration over HTTP

🛠️ Tools & Methods

Splunk – Timeline reconstruction, log correlation

Security Onion (IDS/NSM) – Perimeter telemetry

Wireshark & Firewall logs – Network-level validation

ClamAV / YARA / Sysmon / Wazuh – Threat detection (simulated)

PowerShell / Linux CLI – Forensics & hardening

📑 Lessons Learned

Strengthen email filtering + phishing awareness training

Enforce MFA + strong credential policies for privileged access

Deploy WAF + input validation to protect web applications

Ensure forensic readiness (disk images, log hashing, evidence chain)

👨‍💻 Contributors

Sriram R

Leela Pavan (me)

Shalem Raju

SriVarsha A

Junaid M

Phanindhar Reddy K

Master’s in Cybersecurity & Digital Forensics – University at Albany (Spring 2025)

📄 License

Licensed under CC BY-NC-ND 4.0.
You may share this project with attribution, but commercial use or modifications are not permitted.

👉 This way, it looks like your own repo, while giving full credit to your team.
