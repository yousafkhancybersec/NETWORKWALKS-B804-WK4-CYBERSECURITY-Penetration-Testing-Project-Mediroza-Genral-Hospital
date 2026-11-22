# NETWORKWALKS-B804-WK4-CYBERSECURITY-Penetration-Testing-Project-Mediroza-General-Hospital
# NetworkWalks – Week 04
## Web Application Penetration Testing – Mediroza General Hospital

**A Black-Box Web Application Security Assessment**

---

## Project Overview

This repository documents my Week 04 cybersecurity project completed as part of the NetworkWalks training program.

The project involved conducting a black-box web application security assessment of **Mediroza General Hospital**, focusing on identifying potential security weaknesses, evaluating their impact, documenting technical evidence, and providing remediation recommendations.

The assessment was conducted using Kali Linux, OWASP ZAP, and supporting reconnaissance and security-testing utilities.

The primary objective was to evaluate the security of publicly accessible web application components and identify weaknesses that could affect application security, authentication, and the confidentiality of sensitive information.

## Project Information

| Category | Details |
|---|---|
| Project | Web Application Penetration Testing |
| Training Program | NetworkWalks |
| Week | Week 04 |
| Batch | B804 |
| Prepared By | Yousaf Shafi ullah Khan |
| Target | `https://medirozahospital.com` |
| Assessment Type | Black-Box Security Assessment |
| Operating System | Kali Linux |
| Primary Testing Tool | OWASP ZAP |

## Assessment Objectives

- Perform passive reconnaissance and identify publicly accessible application components.
- Examine web application entry points and authentication mechanisms.
- Identify potential SQL injection vulnerabilities.
- Review directory exposure and application information disclosure.
- Evaluate the security of password-protected PDF documents.
- Analyze findings and assess their potential security impact.
- Document testing evidence and prepare a professional penetration testing report.
- Recommend appropriate security controls and remediation measures.

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| OWASP ZAP | Web application vulnerability assessment |
| WHOIS | Domain registration information |
| DIG | DNS enumeration and record analysis |
| cURL | HTTP response and header inspection |
| OpenSSL | TLS certificate inspection |
| Browser Developer Tools | Web application inspection |
| NetworkWalks Hash Generator | PDF hash extraction and analysis |
| NetworkWalks Password Cracker | Password-strength assessment in the project lab workflow |

## Key Security Findings

The assessment evidence identified the following security issues:

### 1. SQL Injection – Authentication Bypass
- Affected endpoint: `/patient/login.php`
- Affected parameter: `username`
- CWE-89: Improper Neutralization of Special Elements used in an SQL Command.
- OWASP ZAP reported a MySQL SQL injection alert.
- Manual testing evidence indicated authentication bypass and subsequent access to the patient portal.

### 2. Directory Listing Exposure
- Patient and staff application paths exposed directory index pages.
- Application files and directory structure were visible.
- This may disclose information useful for further reconnaissance.

### 3. Confidential Patient Document Exposure
- Evidence showed access to laboratory report entries through the patient portal.
- The assessment demonstrated the potential confidentiality impact of unauthorized access to medical documents.

### 4. Weak PDF Password Protection
- PDF password hashes were extracted for assessment.
- Password-recovery demonstrations indicated weaknesses in the protection of the tested documents.

### 5. Database Error Information Disclosure
- Detailed MySQL error information was displayed in the patient login response.
- This could reveal internal application and database implementation details.

### 6. HTTP Security Header Hardening Gaps
- Several recommended browser security headers were not observed during the recorded response-header inspection.
- These included HSTS, Content-Security-Policy, X-Content-Type-Options, and other defense-in-depth headers.

## Methodology

The assessment followed a structured penetration-testing workflow:

1. **Reconnaissance:** Collected domain, DNS, HTTP, and TLS information.
2. **Application Discovery:** Reviewed publicly accessible pages and application entry points.
3. **Vulnerability Assessment:** Used OWASP ZAP to identify potential web application weaknesses.
4. **Manual Evidence Review:** Examined application responses and documented relevant testing evidence.
5. **Impact Assessment:** Evaluated the potential consequences of identified weaknesses.
6. **Reporting:** Prepared a technical report containing findings, severity assessments, evidence references, and remediation recommendations.

## Recommended Remediation

The following security improvements are recommended:

- Implement parameterized SQL queries and prepared statements.
- Strengthen authentication and enforce server-side authorization.
- Disable directory indexing on sensitive application paths.
- Store confidential documents outside the public web root.
- Verify user ownership before allowing report downloads.
- Avoid weak or predictable PDF passwords.
- Suppress detailed database errors in production environments.
- Configure appropriate HTTP security headers.
- Monitor authentication attempts and sensitive document access.
- Conduct regular security assessments and controlled retesting.

## Project Deliverables

This repository contains project documentation and supporting evidence:

- `WK4_Mediroza_Penetration_Testing_Report.pdf` – Penetration testing report.
- `Screenshots/` – Assessment screenshots and evidence documentation.
- Supporting project files – Related assessment materials.

Refer to the final penetration testing report for detailed findings, technical observations, risk analysis, and remediation recommendations.

## Skills Demonstrated

- Web Application Security Testing
- Black-Box Penetration Testing
- OWASP ZAP
- SQL Injection Analysis
- Authentication Security Assessment
- Directory Listing Analysis
- Information Disclosure Assessment
- PDF Security and Password-Strength Analysis
- DNS and WHOIS Reconnaissance
- HTTP Security Header Analysis
- Technical Documentation and Reporting

## Disclaimer

This repository is intended for educational and authorized cybersecurity assessment purposes.

All testing activities should be performed only with appropriate authorization and within the defined scope of engagement.

Sensitive information, patient records, credentials, recovered passwords, and private data must not be publicly disclosed. Scanner-generated alerts should be distinguished from manually validated findings.

---

**Prepared by:** Yousaf Shafi ullah Khan  
**Program:** NetworkWalks Cybersecurity Training  
**Batch:** B804  
**Project:** Week 04 – Web Application Penetration Testing
