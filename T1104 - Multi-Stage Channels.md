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
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..| 
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..|
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..| 
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..| 
|File Monitoring, Process Monitoring, etc..| Sysmon, WinEvent, PowerShell, etc..|

---

## SPECIFIC EVENTS

| Source | EventID | EventField | Details | Reference | 
|:---:|:---:|:---:|:---:|:---:|
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |
| Sysmon, WinEvent, PowerShell | ID | Field, ALL | Short Description or Strings | \[Author Name\](link) |

---

## DATA ANALYTICS

| Analytic Type | Analytic Logic | Analytic Data Object |
|:---:|---|:---:|
| Behavioral Analytics, Situational Awareness, Anomaly/Outlier |  process_name = xxx AND process_command_line=xxx WHERE xxxxx  | Data Objects... |

---

## HUNTER NOTES
* Host data that can relate unknown or suspicious process activity using a network connection is important to supplement any existing indicators of compromise based on malware command and control signatures and infrastructure. Relating subsequent actions that may result from Discovery of the system and network information or Lateral Movement to the originating process may also yield useful data.

---

## RECOMMENDED HUNTING TECHNIQUES

- [X] Grouping
- [X] Searching
- [ ] Clustering
- [X] Stack Counting
- [ ] Scatter Plots
- [ ] Box Plots
- [X] Isolation Forests

---