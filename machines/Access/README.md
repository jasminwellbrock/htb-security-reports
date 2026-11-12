# Access – Hack The Box

**Platform:** Hack The Box  
**OS:** Windows  
**Difficulty:** Easy  
**Status:** Retired  
**Report:** [Access Security Assessment Report](./Access_Security_Assessment_Report.pdf)

## Overview

Access is a retired Windows machine that demonstrates how exposed backup files and insecure credential management can lead to full system compromise.

The assessment begins with anonymous FTP access, followed by offline analysis of backup data and an Outlook mailbox. Credentials recovered from the mailbox provide an initial foothold through Telnet.

Further Windows enumeration reveals stored Administrator credentials that can be abused through `runas /savecred`, ultimately allowing execution as `ACCESS\Administrator`.

## Skills Demonstrated

- Network reconnaissance and service enumeration
- Anonymous FTP enumeration
- Backup file analysis
- Outlook mailbox analysis
- Credential discovery
- Telnet authentication
- Windows enumeration
- Windows Credential Manager
- `runas /savecred` abuse
- PowerShell scripting
- Nishang reverse shells
- Privilege escalation to Administrator

## Key Findings

| Finding | CVSS v3.1 | Severity |
|---|---:|---|
| Anonymous FTP – Sensitive Backup Exposure | 7.5 | High |
| Stored Administrator Credentials – `runas /savecred` | 7.8 | High |

*CVSS scores are indicative assessments of the demonstrated attack path.*

## Tools Used

- Nmap
- FTP
- 7-Zip
- Telnet
- Windows CMD
- PowerShell
- Nishang
- Netcat
- Python HTTP Server

## Disclaimer

This report documents a controlled Hack The Box training environment. No real-world systems were targeted. Sensitive credentials and flag values have been redacted.
