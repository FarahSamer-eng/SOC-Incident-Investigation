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

The web access logs showed repeated POST requests to `/wp-login.php` originating from `10.10.243.134`.

The User-Agent identified the tool as `WPScan v3.8.28`.

## Investigation Classification

The activity was classified as suspicious automated web activity targeting a WordPress login endpoint.
