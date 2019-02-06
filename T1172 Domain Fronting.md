# Domain Fronting

<BR>
 
## Description
Domain fronting takes advantage of routing schemes in Content Delivery Networks (CDNs) and other services which host multiple domains to obfuscate the intended destination of HTTPS traffic or traffic tunneled through HTTPS. [1] The technique involves using different domain names in the SNI (Server Name Indicator) field of the TLS header and the Host field of the HTTP header. If both domains are served from the same CDN, then the CDN may route to the address specified in the HTTP header after unwrapping the TLS header. A variation of the the technique, "domainless" fronting, utilizes a SNI field that is left blank; this may allow the fronting to work even when the CDN attempts to validate that the SNI and HTTP Host fields match (if the blank SNI fields are ignored).

For example, if domain-x and domain-y are customers of the same CDN, it is possible to place domain-x in the TLS header and domain-y in the HTTP header. Traffic will appear to be going to domain-x, however the CDN may route it to domain-y.

## ASSOCIATED MITRE ATT&CK TACTIC(S)
- [TA0011](https://attack.mitre.org/tactics/TA0011/) (Command and Control)

## ASSOCIATED MITRE ATT&CK TACTIC(S)- Technique: 
- [T1065](https://attack.mitre.org/techniques/T1172/) (Domain Fronting)

---

## Recommended Data Sources

| ATT&CK Data Source |
|---------|
| Web proxy logs | 
| Full packet capture |

---

## SPECIFIC EVENTS

| Source | EventID | EventField | Details | Reference | 
|:---:|:---:|:---:|:---:|:---:|

---

## DATA ANALYTICS

| Analytic Type | Analytic Logic | Analytic Data Object |
|:---:|---|:---:|

---

## Hunter Notes
* Detection of this technique can be difficult without additional indications of an attack.
* HTTPS Traffic - Must be able to first, break and inspect TLS encrypted traffic. A clear 
indication of domain fronting would be differences in the Server Name Indicator and the 
HTTP header host field after decrypting the traffic.
* HTTP Traffic - An indication of Domain fronting would be a mismatch of the 
"Host" field from the domain a request is being sent to in the URI field.
 
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
