# Valentine

Penetration testing report for the retired Hack The Box Machine **Valentine**.

## Overview

This report documents a black-box security assessment of the retired Hack The Box machine Valentine.

The assessment covers the identification and exploitation of the Heartbleed vulnerability (CVE-2014-0160), recovery of SSH private-key material, SSH authentication, local enumeration, and privilege escalation through an accessible privileged tmux session.

## Findings

| Severity | Finding | CVE |
|---|---|---|
| Critical (indicative) | Heartbleed Memory Disclosure | CVE-2014-0160 |
| High (indicative) | SSH Private Key Exposed Through Web Directory | — |
| Critical (indicative) | Accessible Privileged tmux Session | — |

## Attack Path

```text
Service Enumeration
        ↓
Heartbleed Detection
        ↓
TLS Memory Disclosure
        ↓
SSH Private Key Recovery
        ↓
SSH Access as hype
        ↓
Local Enumeration
        ↓
Accessible tmux Socket
        ↓
Attach to Privileged Session
        ↓
Root Access
```

## Skills Demonstrated

- Network Enumeration
- Nmap Vulnerability Scanning
- TLS Vulnerability Analysis
- Heartbleed (CVE-2014-0160)
- Metasploit Framework
- Memory Dump Analysis
- SSH Key Analysis
- Web Directory Enumeration
- SSH Authentication
- Linux Enumeration
- tmux Analysis
- Linux Privilege Escalation
- Technical Security Reporting

## Report

**[View the Full Security Assessment Report](./Valentine_Security_Assessment_Report.pdf)**

The report contains the assessment methodology, technical findings, exploitation walkthrough, evidence screenshots, remediation recommendations, and supplementary evidence.

---

**Platform:** Hack The Box  
**Type:** Machine  
**Status:** Retired  
**Focus:** Penetration Testing · Vulnerability Assessment · Privilege Escalation
