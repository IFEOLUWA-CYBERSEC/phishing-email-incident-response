

## Project Overview

This project simulates a real-world SOC phishing investigation.  
The objective was to analyze a suspicious email, extract indicators of compromise (IOCs), assess risk, and recommend remediation actions following SOC playbooks.

## Purpose & Ethical Use

This repository documents a phishing email incident-response investigation conducted for defensive security research, SOC training, and educational purposes only.

All materials are intended for lawful use in controlled, isolated environments.  
Do **not** use any content in this repository to conduct real phishing campaigns, target real users, or test systems without explicit written authorization.

The focus of this project is detection, analysis, documentation, and remediation of phishing threats.

## Tools Used
- VirusTotal
- ANY.RUN
- WHOIS
- MITRE ATT&CK Framework

## Investigation Steps
- Email header analysis
- IOC extraction (IP, domain, email address)
- Threat intelligence enrichment
- Risk assessment
- MITRE ATT&CK mapping
- Incident response recommendations

## Key Findings
- Phishing email leveraging social engineering techniques
- Clean IP reputation used to evade detection
- Medium to High risk to users if interacted with

## Outcome
A full incident report documenting analysis, response actions, and lessons learned, suitable for SOC Tier 1 workflows.

## Skills Demonstrated
- Phishing analysis
- Incident response
- Threat intelligence
- SOC documentation

### Documentation
- 📄 [Incident Report](incident-report.md)
- 🕒 [Incident Timeline](incident-timeline.md)

## Screenshots & Evidence

### Email Header Analysis
![Email Header Analysis](screenshots/Screenshot%202026-01-28%20140546.png)
This screenshot shows the analysis of SMTP headers used to identify the email origin and delivery path.

### IOC Enrichment – VirusTotal
![VirusTotal IP Analysis](screenshots/Screenshot%202026-01-28%20153857.png)
This screenshot shows the analysis of SMTP headers used to identify the email origin and delivery path.

### GitHub Project Structure
![Repository Overview](screenshots/Screenshot%202026-01-28%20154020.png)
This screenshot shows the analysis of SMTP headers used to identify the email origin and delivery path.

Note: This repository is documentation-based and does not publish releases or packages.
