# Phishing Email Incident Report

## Case Overview
This project documents the analysis of a suspected phishing email as part of a SOC-style investigation. The goal is to extract indicators of compromise (IOCs), assess risk, and recommend response actions.

## Evidence Acquisition & Secure Artifact Handling
The phishing email contained a password-protected archive, a common technique used by attackers to evade email security scanners.

Before analysis, the attachment was handled carefully to avoid accidental execution. The archive required a password provided within the email body, which was used to safely extract the contents for further investigation.

## 5. Sample Acquisition & Safe Handling

### 5.1 Source of Phishing Samples

The phishing email samples used in this investigation were obtained from **Malware-Traffic-Analysis.net**, a well-known platform used by cybersecurity professionals for malware and phishing research. The platform provides sanitized but realistic samples intended strictly for educational and defensive analysis.

The selected dataset contained multiple phishing email examples packaged in a compressed archive for controlled distribution.

---

### 5.2 Password-Protected Archive Verification

To reduce the risk of accidental execution or automated scanning, the phishing samples were distributed within a password-protected ZIP archive. Before extraction, the password scheme was verified from the website’s **About** page.

The website specifies that password-protected archives follow this format:


For the selected archive dated **May 5, 2020**, the verified password was:


This verification step ensured the archive was accessed safely and intentionally.

---

### 5.3 Secure Extraction Using 7-Zip

The compressed archive was extracted using **7-Zip** in a controlled environment. No files were executed during this process. The correct password (`infected_20200505`) was supplied manually to extract the contents securely.

This step allowed safe access to the phishing artifacts while maintaining proper malware-handling precautions.

---

### 5.4 Extracted Email Artifacts

After successful extraction, multiple phishing email samples in `.eml` format were identified. These email files represent real-world phishing attempts and were prepared for further analysis, including header inspection, content review, and indicator extraction.

The extracted files include:

- 2020-05-05-phishing-email-example-01.eml  
- 2020-05-05-phishing-email-example-02.eml  
- 2020-05-05-phishing-email-example-03.eml  
- 2020-05-05-phishing-email-example-04.eml  

These artifacts form the basis for subsequent phishing analysis and indicator-of-compromise (IOC) development.





### 5.2 Password-Protected Archive Verification
The phishing samples were provided in a password-protected ZIP archive to prevent accidental execution of malicious files. The password format was verified from the website’s About page before extraction.


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

## MITRE ATT&CK Mapping

Based on the analysis, the phishing activity aligns with the following MITRE ATT&CK techniques:

- **T1566.001 – Phishing: Spearphishing Attachment**
- **T1566.002 – Phishing: Spearphishing Link**

The attacker attempted to socially engineer the recipient into interacting with malicious content to obtain credentials or execute further payload delivery.

## Response and Remediation Actions

The following actions are recommended to contain and remediate the phishing incident:

- Block the sender IP address and domain at the email gateway and firewall.
- Remove the phishing email from all user inboxes.
- Reset credentials for any users who interacted with the email.
- Monitor for additional emails originating from related infrastructure.
- Conduct user awareness training to prevent similar phishing attempts.

## Incident Conclusion

This incident involved a phishing email designed to deceive users and potentially harvest credentials.  
Although the sending IP address was not flagged by reputation-based tools, contextual analysis confirms malicious intent.

Timely detection, IOC enrichment, and user awareness are critical to reducing the impact of similar phishing campaigns in the future.
