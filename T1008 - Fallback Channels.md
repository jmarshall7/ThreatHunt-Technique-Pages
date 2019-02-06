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

| ATT&CK Data Source | Event Log |
|:---:|:---:|
| Packet Capture | Packet capture / network traffic analyzer (wireshark/tcpdump)|
| Netflow/Enclave Netflow | Netflow capture software/appliance|
| Process Monitoring | Sysmon |
| Process Use of Network | Sysmon |

---

## SPECIFIC EVENTS

| Source | EventID | EventField | Details | Reference | 
|:---:|:---:|:---:|:---:|:---:|
| N/A | N/A | N/A | N/A | N/A |

---

## DATA ANALYTICS

| Analytic Type | Analytic Logic | Analytic Data Object |
|:---:|---|:---:|
| Anomaly/Outlier | process_name = xxx AND netconn_count:[1 TO *] | Process Execution |

---

## HUNTER NOTES
* Analyze network data for unusual amounts of data to/from endpoints.
* Processes making network connections that do not normally have network communication or have never been seen before. Long-   tail analysis may be best approach here. 
* Analyze packet contents to detect communications that do not follow the expected protocol behavior for the port that is     being used. 
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
