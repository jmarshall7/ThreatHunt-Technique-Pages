# Multi-Stage Channels

<BR>

## DESCRIPTION
Adversaries may create multiple stages for command and control that are employed under different conditions or for certain functions. Use of multiple stages may obfuscate the command and control channel to make detection more difficult.

## ASSOCIATED MITRE ATT&CK TACTIC(S)
- [TA0011 - Command And Control](https://attack.mitre.org/tactics/TA0011/)

## ASSOCIATED MITRE ATT&CK TECHNIQUE(S)
- [T1104 - Multi-Stage Channels](https://attack.mitre.org/techniques/T1104/)

---

## RECOMMENDED DATA SOURCES

| ATT&CK Data Source | Event Log |
|:---:|:---:|
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..|

---

## SPECIFIC EVENTS

| Source | EventID | EventField | Details | Reference | 
|:---:|:---:|:---:|:---:|:---:|
| Packet Capture | Packet capture / network traffic analyzer (wireshark/tcpdump)|
| Netflow/Enclave Netflow | Netflow capture software/appliance|
| Process Monitoring | Sysmon |
| Process Use of Network | Sysmon |

---

## DATA ANALYTICS

| Analytic Type | Analytic Logic | Analytic Data Object |
|:---:|---|:---:|
| Anomaly/Outlier | process_name = xxx AND netconn_count:[1 TO * ] | Process Execution |

---

## HUNTER NOTES
* Host data that can relate unknown or suspicious process activity using a network connection is important to supplement any existing indicators of compromise based on malware command and control signatures and infrastructure. Relating subsequent actions that may result from Discovery of the system and network information or Lateral Movement to the originating process may also yield useful data.
* Hunting out Multi-stage C2 channels can be a challenging task especially at the endpoint. We would most-likely at this point in time have to rely on IOC feeds in hopes of identifying re-used C2 infrastructure. Beyond that hunts for process executions with suspicious network connections could possibly uncover this technique. Even with identifying suspicious process network connections it would take more amplifying information to determine that Multi-stage channel technique is being execuited.

---

## RECOMMENDED HUNTING TECHNIQUES

- [ ] Grouping
- [X] Searching
- [ ] Clustering
- [X] Stack Counting
- [ ] Scatter Plots
- [ ] Box Plots
- [X] Isolation Forests

---
