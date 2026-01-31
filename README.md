

## Project Overview

This project simulates a real-world SOC phishing investigation.  
The objective was to analyze a suspicious email, extract indicators of compromise (IOCs), assess risk, and recommend remediation actions following SOC playbooks.

# Phishing Email Incident Response — SOC Case Study

## TL;DR
A defensive Security Operations Center (SOC) case study documenting the end-to-end investigation of a real-world phishing email, including header analysis, IOC extraction, threat enrichment, MITRE ATT&CK mapping, and remediation recommendations.

## Quick Facts
- **Role:** SOC Analyst / Incident Responder (solo)
- **Incident Type:** Phishing (credential harvesting)
- **Tools:** Email header analysis, VirusTotal, WHOIS, MITRE ATT&CK, Python (email parsing), Jupyter
- **Key Outputs:** Sanitized incident report, structured IOCs, detection recommendations
- **Time to Complete:** ~6 hours (analysis, enrichment, reporting)
- **Focus Areas:** Phishing analysis, evidence handling, detection engineering, reporting

## Why This Project
This project demonstrates practical SOC skills used in real environments: identifying phishing infrastructure, extracting and enriching indicators, mapping attacker behavior, and producing clear, professional incident documentation — while applying proper evidence hygiene and ethical handling.

> ⚠️ **Ethical Notice:** All sensitive artifacts (passwords, raw `.eml` files, and identifying information) have been sanitized or withheld. Raw evidence is stored privately and not published.

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
