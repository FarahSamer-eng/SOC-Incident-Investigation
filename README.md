# SOC Incident Investigation

## Overview

This project documents a hands-on SOC investigation using Splunk to analyze security logs and identify suspicious activity.

The investigation was performed in a simulated environment as part of practical cybersecurity training.

## Objectives

- Analyze security logs using a SIEM
- Identify suspicious authentication and network activity
- Investigate potential brute-force attacks
- Identify indicators of compromise
- Document findings and recommended mitigations

## Tools & Technologies

- Splunk
- SIEM
- Windows Event Logs
- Linux Logs
- Web/Apache Access Logs
- TryHackMe Lab Environment

## Investigation Areas

- Windows log analysis
- Linux authentication analysis
- Web log analysis
- Brute-force detection
- Suspicious process investigation
- Persistence analysis

## Key Findings

The investigation identified several suspicious activities, including:

- Brute-force activity targeting a WordPress login endpoint
- Suspicious process execution
- Suspicious account activity
- Persistence through a scheduled task
- Suspicious web requests

## Skills Demonstrated

- Log Analysis
- SIEM Investigation
- Incident Detection
- Threat Investigation
- IOC Identification
- Basic Incident Response
- Security Documentation

## Evidence

### WPScan Web Attack Investigation

Evidence from Splunk showing repeated requests to the WordPress login endpoint and identification of WPScan as the User-Agent.

![WPScan Investigation Evidence](task6-wpscan-evidence.png)


## Investigation Evidence

### Web Attack Detection

The investigation identified repeated requests targeting the WordPress login endpoint.

**Source IP:** `10.10.243.134`  
**Target:** `/wp-login.php`  
**Tool:** `WPScan v3.8.28`

![WPScan Evidence](task6-wpscan-evidence.png)

## Investigation Workflow

1. Collected and reviewed web access logs.
2. Identified the most requested URI.
3. Investigated the source IP address.
4. Analyzed the User-Agent to identify the attack tool.
5. Classified the suspicious activity.
6. Documented indicators of compromise.
7. Recommended mitigation measures.

## Project Files

- [Investigation Report](Investigation-Report.md)
- [Indicators of Compromise](findings/indicators-of-compromise.md)
