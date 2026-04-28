# SOC-Brute-Force-Detection-Sentinel
Detection and Investigation of a brute-force attacks using Microsoft Sentinel (SOC Lab project)
# 🚨 Brute Force Attack Detection using Microsoft Sentinel

## 📌 Overview
This project demonstrates the detection and investigation of a brute-force attack using Microsoft Sentinel in a SOC lab environment.

## 🎯 Objective
To simulate unauthorized login attempts and detect them using SIEM capabilities.

## 🛠️ Tools Used
- Microsoft Sentinel
- Azure Virtual Machine
- Log Analytics Workspace
- KQL (Kusto Query Language)

## ⚔️ Scenario
A brute-force attack was simulated by entering incorrect passwords multiple times on a Windows VM.

## 🔍 Detection
The following KQL query was used:

```kql
Event
| where EventID == 4625

## 🧠 Investigation Findings
- Detected multiple failed login attempts within a short time window
- Activity targeted VM: **vm-soc-win01**
- Pattern suggests automated brute-force attack behavior
- No successful login observed following failed attempts

## 🕒 Attack Timeline
- Initial failed login detected at 08:50
- Multiple attempts occurred within 5 minutes
- No successful authentication recorded

## 🚨 Severity Assessment
**Medium to High** – Indicates a potential brute-force attack that could lead to unauthorized access

## 🧬 MITRE ATT&CK Mapping
- Technique: Brute Force
- ID: T1110

## 🛡️ Response Actions
- Enabled account lockout policy
- Recommended Multi-Factor Authentication (MFA)
- Configured alerting for repeated login failures
- Suggested monitoring for further suspicious activity


## 📊 Detection Screenshot
![<img width="1683" height="880" alt="Screenshot 2026-04-24 131650" src="https://github.com/user-attachments/assets/b9860f86-93f8-4b32-8a85-d2280155c7a0" />
](screenshots/detection.png)

## 📊 Analysis Screenshot
![<img width="1686" height="412" alt="Screenshot 2026-04-24 131114" src="https://github.com/user-attachments/assets/200effb1-8149-4442-9ee4-35cf06d72940" />
<img width="1744" height="790" alt="Screenshot 2026-04-24 131001" src="https://github.com/user-attachments/assets/8386bf90-c505-4d76-8c9a-86cd31989873" />
](screenshots/analysis.png)

## 🧠 Conclusion
This project successfully demonstrated the detection and investigation of a brute-force attack using Microsoft Sentinel. It highlights the importance of monitoring authentication logs and implementing proactive security controls.

## 📄 Full Report
[View Full Report](report/Brute-Force-Detection.pdf)
