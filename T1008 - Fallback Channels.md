# Fallback Channels

<BR>

## DESCRIPTION
Adversaries may use fallback or alternate communication channels if the primary channel is compromised or inaccessible in order to maintain reliable command and control and to avoid data transfer thresholds.
## ASSOCIATED MITRE ATT&CK TACTIC(S)
- [TA0011 - Command and Control](https://attack.mitre.org/tactics/TA0011/)

## ASSOCIATED MITRE ATT&CK TECHNIQUE(S)
- [T1008 - Fallback Channels](https://attack.mitre.org/techniques/T1008/)

---

## RECOMMENDED DATA SOURCES

| ATT&CK Data Source |
|:---:|
| Packet capture |
| Netflow/Enclave Netflow |
| Process Monitoring |
| Process Use of Network | 

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
* Analyze network data for unusual amounts of data to/from endpoints.
* Processes making network connections that do not normally have network communication or have never been seen before. Long-   tail analysis may be best approach here. 
* Analyze packet contents to detect communications that do not follow the expected protocol behavior for the port that is     being used. 
---

## RECOMMENDED HUNTING TECHNIQUES

- [ ] Grouping
- [ ] Searching
- [ ] Clustering
- [ ] Stack Counting
- [ ] Scatter Plots
- [ ] Box Plots
- [ ] Isolation Forests

---
