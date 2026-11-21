# Admirer

Penetration testing report for the retired Hack The Box Machine **Admirer**.

## Overview

This report documents a black-box security assessment of the retired Hack The Box machine Admirer.

The assessment covers sensitive information disclosure through web and FTP services, exploitation of an arbitrary file read vulnerability in Adminer 4.6.2 (CVE-2021-43008), credential recovery, SSH access, and Linux privilege escalation through sudo environment variable manipulation and Python import hijacking.

## Findings

| Severity | Finding | CVE |
|---|---|---|
| High (indicative) | Sensitive Credentials and Personal Contact Data Exposed | — |
| High (indicative) | Adminer Arbitrary File Read | CVE-2021-43008 |
| High (indicative) | Credential Reuse Enabling SSH Access | — |
| Critical (indicative) | Sudo SETENV Permission Enables Python Import Hijacking | — |

## Attack Path

```text
Network Enumeration
        ↓
Web and FTP Enumeration
        ↓
Sensitive File and Credential Discovery
        ↓
Adminer 4.6.2 Arbitrary File Read
        ↓
Application Configuration Disclosure
        ↓
Credential Recovery
        ↓
SSH Access as waldo
        ↓
Sudo Configuration Enumeration
        ↓
SETENV Permission Abuse
        ↓
Python Import Hijacking via PYTHONPATH
        ↓
SUID Bash Creation
        ↓
Root Access
```

## Skills Demonstrated

- Network Enumeration
- Web Application Enumeration
- FTP Enumeration
- Directory Discovery with Dirsearch
- Adminer Security Assessment
- Arbitrary File Read Analysis
- CVE Research and Validation
- Credential Discovery and Analysis
- SSH Authentication
- Linux Enumeration
- Sudo Misconfiguration Analysis
- Python Import Hijacking
- Environment Variable Manipulation
- SUID Exploitation
- Linux Privilege Escalation
- Technical Security Reporting

## Report

**[View the Full Security Assessment Report](./Admirer_Security_Assessment_Report.pdf)**

The report contains the assessment methodology, technical findings, exploitation walkthrough, evidence screenshots, remediation recommendations, and supplementary evidence.

---

**Platform:** Hack The Box  
**Type:** Machine  
**Status:** Retired  
**Focus:** Web Application Security · Adminer · Credential Discovery · Python Import Hijacking · Linux Privilege Escalation
