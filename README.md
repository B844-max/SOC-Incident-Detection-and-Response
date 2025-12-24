📌 Overview

This repository documents a hands-on Security Operations Center (SOC) lab focused on incident detection, investigation, and response using real endpoint and network logs. The project simulates common attack scenarios and demonstrates how a SOC analyst detects threats using SIEM correlation, endpoint telemetry, and MITRE ATT&CK mapping.

The goal of this lab is to move beyond theoretical learning and showcase practical SOC-ready skills.

🧱 Lab Architecture

Endpoint: Windows VM

Logging & Telemetry:

Sysmon (Process, DNS, and system activity)

Windows Security Event Logs

SIEM: Splunk Enterprise

Log Forwarding: Splunk Universal Forwarder

Analysis: Splunk Search & Correlation

Framework: MITRE ATT&CK

Windows Endpoint
   │
   ├─ Sysmon + Windows Event Logs
   │
Splunk Universal Forwarder
   │
Splunk Enterprise (SIEM)
   │
Detection → Investigation → Response

🛑 Incident Scenarios Covered
1️⃣ Brute Force Authentication Attack

Detected repeated failed login attempts

Correlated authentication events to identify attack patterns

Logs used:

Windows Security Event ID 4625 / 4624

MITRE ATT&CK:

T1110 – Brute Force

📂 Folder: Incident-1-Brute-Force/

2️⃣ PowerShell Living-off-the-Land (LOLBins)

Detected suspicious PowerShell execution

Analyzed process creation behavior

Focused on behavioral detection rather than single indicators

Logs used:

Sysmon Event ID 1 (Process Create)

MITRE ATT&CK:

T1059.001 – PowerShell

📂 Folder: Incident-2-PowerShell-LOLBins/

3️⃣ DNS Beaconing (Command & Control)

Detected suspicious DNS query patterns

Identified potential C2 beaconing behavior

Used SIEM correlation due to DNS caching limitations

Logs used:

Sysmon Event ID 22 (DNS Query)

MITRE ATT&CK:

T1071.004 – DNS Command and Control

📂 Folder: Incident-3-DNS-Beaconing/

🔍 Detection Methodology

For each incident:

Log Collection – Endpoint telemetry ingested into Splunk

Detection Logic – SIEM queries and correlation

Investigation – Contextual analysis (time, frequency, process, user)

MITRE Mapping – Classification of attacker behavior

Response – Recommended containment and monitoring actions

Documentation – Incident reports and evidence

🧠 Key SOC Skills Demonstrated

SIEM monitoring & alert triage

Log analysis and correlation

Endpoint detection using Sysmon

Incident investigation & response

MITRE ATT&CK mapping

Troubleshooting log ingestion issues

Professional incident documentation

🛠 Tools & Technologies

Splunk Enterprise

Splunk Universal Forwarder

Sysmon

Windows Event Logs

Wireshark (supporting analysis)

MITRE ATT&CK Framework

📂 Repository Structure
SOC-Incident-Detection-and-Response/
│
├── Incident-1-Brute-Force/
├── Incident-2-PowerShell-LOLBins/
├── Incident-3-DNS-Beaconing/




Finalize your resume bullets using this repo

Just tell me what you want next 👊
