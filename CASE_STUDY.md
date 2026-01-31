# Case Study: Phishing Email Incident Response (Sanitized)

## Executive Summary
A suspicious email was reported by a user and analyzed to determine whether it represented a phishing threat. Header analysis revealed an external sending infrastructure associated with known malicious activity. Indicators were extracted, enriched, and mapped to attacker techniques. Containment and detection recommendations were produced.

- **Threat Type:** Phishing / Credential Harvesting
- **Severity:** Medium–High (if user interaction occurred)
- **Outcome:** Malicious infrastructure identified, IOCs documented, detection guidance created

---

## My Role & Responsibilities
As the sole analyst, I was responsible for:
- Analyzing the reported phishing email
- Extracting and validating indicators of compromise (IOCs)
- Enriching indicators using open-source threat intelligence
- Mapping attacker behavior to MITRE ATT&CK
- Producing a professional, sanitized incident report

---

## Investigation Methodology

### 1. Evidence Acquisition & Handling
- Obtained the suspicious email in `.eml` format
- Extracted artifacts in a controlled environment
- Preserved original evidence privately
- Sanitized all public outputs to remove credentials and PII

### 2. Email Header Analysis
- Parsed SMTP headers to identify:
  - Sending IP address
  - Relay chain
  - Originating domain
- Identified the earliest external relay as the likely source

### 3. Indicator Extraction
Extracted the following indicator types:
- IP addresses
- Domains
- Sender infrastructure details

Indicators were normalized and validated before enrichment.

### 4. Threat Enrichment
- Queried indicators against VirusTotal and WHOIS
- Identified prior malicious associations
- Assessed reputation and historical activity

### 5. ATT&CK Mapping
Mapped observed behavior to MITRE ATT&CK techniques, including:
- **T1566.001 – Phishing: Spearphishing Attachment**
- **T1566.002 – Phishing: Spearphishing Link**

---

## Containment & Mitigation Recommendations
- Block malicious sender IP and domains at the email gateway
- Search and remove similar messages from user mailboxes
- Reset credentials for potentially impacted users
- Educate users on phishing indicators

---

## Deliverables
- **Sanitized Incident Report:** `incident-report-sanitized.md`
- **Structured IOCs:** `iocs/`
- **Detection Guidance:** Sigma rule example and SIEM logic (planned extension)

---

## Lessons Learned
- Sanitization is critical when publishing real incident material
- Structured IOCs improve reusability and detection
- Clear documentation is as important as technical analysis

This case study reflects how phishing incidents are investigated and documented in a professional SOC environment.
