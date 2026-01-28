# Phishing Email Incident Report

## Case Overview
This project documents the analysis of a suspected phishing email as part of a SOC-style investigation. The goal is to extract indicators of compromise (IOCs), assess risk, and recommend response actions.

## Investigation Status
- Email sample obtained
- Email headers opened and reviewed
- Initial header analysis started

## Evidence Collected
- Raw email headers
- Screenshots of header review
## Email Header Analysis

## Indicators of Compromise (IOCs)

| Type | Value | Description |
|------|-------|-------------|
| IP Address | 173.46.174.49 | Original sending IP identified from email headers |
| Domain | malware-traffic-analysis.net | Sender display domain |
| Domain | mail.nmifi.com | Sending mail server infrastructure |


**From:** brad@malware-traffic-analysis.net  
**Sender Domain:** malware-traffic-analysis.net  

**Sending IP:** 173.46.174.49  
**Sending Mail Server:** mail.nmifi.com  

**Analysis Notes:**
Multiple internal relay headers were observed (127.0.0.1). The earliest public IP address was identified as the original sending source.

## Next Steps
- Complete email header analysis
- Extract IOCs (IP addresses, domains, URLs)
- Analyze indicators using threat intelligence tools
- Map activity to MITRE ATT&CK
- Recommend remediation actions
---

## IOC Enrichment – VirusTotal

The sending IP address `173.46.174.49` was analyzed using VirusTotal.

- Detection Ratio: 0/92
- Country: United States
- Community Score: 0

Although no security vendor flagged the IP as malicious at the time of analysis, its presence in a confirmed phishing email indicates suspicious behavior. Threat actors commonly use clean or residential IP addresses to evade reputation-based detection systems.
## Risk Assessment

This phishing email presents a **Medium to High risk** to the organization.

Potential impact if a user interacted with the email includes:
- Credential harvesting
- Unauthorized account access
- Follow-on phishing attacks
- Potential malware delivery in later stages

The lack of current detection increases the likelihood of successful social engineering.
