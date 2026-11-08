# Curling

Penetration testing report for the retired Hack The Box Machine **Curling**.

## Overview

This report documents a black-box security assessment of the retired Hack The Box machine Curling.

The assessment covers credential discovery through publicly accessible web resources, Joomla administrator access, authenticated PHP execution, credential recovery from a nested backup archive, SSH access, and privilege escalation through an unsafe curl configuration in a privileged cron job.

## Findings

| Severity | Finding |
|---|---|
| High (indicative) | Publicly Accessible Credential Material |
| High (indicative) | Authenticated PHP Execution Through Joomla Template Editing |
| High (indicative) | Floris Credential Recoverable from Nested Backup Archive |
| Critical (indicative) | Root Cron Job Trusts User-Writable curl Configuration |

## Attack Path

```text
Joomla Source Inspection
        ↓
Public secret.txt Discovery
        ↓
Base64 Credential Recovery
        ↓
Joomla Administrator Access
        ↓
Authenticated PHP Execution
        ↓
Initial Access as www-data
        ↓
Nested Backup Archive Reconstruction
        ↓
SSH Access as floris
        ↓
Root Cron Job Enumeration
        ↓
curl Configuration Injection
        ↓
Sudoers Modification
        ↓
Root Access
```
## Skills Demonstrated

- Network Enumeration
- Web Application Assessment
- Joomla Administration
- Credential Discovery
- Base64 Decoding
- PHP Execution
- Linux Enumeration
- Archive Reconstruction
- SSH Authentication
- Process and Cron Analysis
- pspy
- Linux Privilege Escalation
- Technical Security Reporting

## Report

**[View the Full Security Assessment Report](./Curling_Security_Assessment_Report.pdf)**

The report contains the assessment methodology, technical findings, exploitation walkthrough, evidence screenshots, remediation recommendations, and supplementary evidence.

---

**Platform:** Hack The Box  
**Type:** Machine  
**Status:** Retired  
**Focus:** Web Application Security · Credential Recovery · Linux Privilege Escalation
