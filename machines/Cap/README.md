# Cap

Penetration testing report for the retired Hack The Box Machine **Cap**.

## Overview

This report documents a black-box security assessment of the retired Hack The Box machine Cap.

The assessment demonstrates the identification and exploitation of an Insecure Direct Object Reference (IDOR), analysis of captured network traffic, credential reuse, SSH access, Linux capability abuse, and privilege escalation to root.

## Findings

| Severity | Finding | CVSS |
|---|---|---:|
| High | Python Binary with CAP_SETUID Capability Allows Privilege Escalation to Root | 7.8 |
| High | Insecure Direct Object Reference Allows Unauthorized Access to PCAP Captures | 7.5 |

## Attack Path

```text
Unauthenticated Access
        ↓
Security Dashboard
        ↓
IDOR → Unauthorized PCAP Access
        ↓
PCAP Analysis
        ↓
FTP Credentials
        ↓
SSH Access as nathan
        ↓
CAP_SETUID on Python 3.8
        ↓
Privilege Escalation
        ↓
Root
