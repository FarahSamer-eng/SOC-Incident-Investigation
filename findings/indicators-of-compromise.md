# Indicators of Compromise

## Web Attack Investigation

| Indicator | Value |
|---|---|
| Source IP | 10.10.243.134 |
| Target URI | /wp-login.php |
| HTTP Method | POST |
| Attack Tool | WPScan v3.8.28 |
| Log Source | Web Access Logs |

## Evidence

The investigation identified repeated POST requests targeting the WordPress login endpoint.

The source IP was `10.10.243.134`.

The User-Agent identified the tool as `WPScan v3.8.28`.

## Classification

The activity was classified as automated web activity targeting a WordPress login endpoint.

## Recommendations

- Monitor repeated authentication attempts.
- Restrict suspicious source IP addresses.
- Enable rate limiting on the login endpoint.
- Review WordPress authentication logs regularly.
