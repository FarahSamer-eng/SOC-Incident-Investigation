# SOC Incident Investigation Report

## 1. Investigation Overview

This investigation analyzes simulated security logs using Splunk SIEM to identify and investigate suspicious activity.

The investigation was performed in a controlled training environment using the TryHackMe Log Analysis with SIEM room.

## 2. Tools


- Splunk
- SIEM
- Web Access Logs
- TryHackMe Training Environment

## 3. Incident Identified

A high volume of requests was identified against the WordPress login endpoint:

`/wp-login.php`

The activity originated from:

`10.10.243.134`

The requests were primarily HTTP POST requests targeting the login endpoint.

## 4. Attack Tool
The User-Agent identified the scanning tool as:

`WPScan v3.8.28`

Example log evidence:

`"POST /wp-login.php HTTP/1.1" 200 ... "WPScan v3.8.28"`

## 5. Analysis

The repeated requests to the WordPress login endpoint, combined with the identified security scanning tool, indicate suspicious automated activity targeting the web application.

The activity was classified as:

**Brute Force Activity**

## 6. Indicators of Compromise

| Indicator | Value |
|---|---|
| Source IP | 10.10.243.134 |
| Target URI | /wp-login.php |
| HTTP Method | POST |
| Tool | WPScan v3.8.28 |
| Log Source | Apache/Web Access Logs |

## 7. Recommended Mitigations

- Implement rate limiting on authentication endpoints.
- Enable multi-factor authentication.
- Monitor repeated authentication requests.
- Restrict unnecessary access to administrative login pages.
- Monitor and investigate suspicious User-Agent strings.
- Use WAF rules to detect automated scanning activity.

## 8. Conclusion

The investigation demonstrated how SIEM-based log analysis can be used to identify suspicious web activity, determine the source of the activity, identify the attack tool, and document relevant indicators of compromise.
