# Vulnerability Assessment and Penetration Testing (VAPT) Report  
**Targets:** DVWA, PortSwigger Web Security Academy, Zero WebAppSecurity  
**Author:** Abishek V  
**Date:** 10.08.2025  

---

##  Overview
This repository contains a **combined Vulnerability Assessment and Penetration Testing (VAPT) report** performed against three intentionally vulnerable web applications:

- **DVWA** – Damn Vulnerable Web Application  
- **PortSwigger Web Security Academy Labs**  
- **Zero WebAppSecurity**  

The engagement identified **10 vulnerabilities** across the three applications, ranging from **Critical** to **Low** severity, with detailed exploitation steps, impacts, and remediation measures.

---

##  Objectives
The goal of this VAPT engagement was to:
- Identify and classify security vulnerabilities in the target applications.
- Demonstrate exploitability through proof-of-concept attacks.
- Recommend actionable remediation steps to improve security posture.
- Map findings to industry standards such as **OWASP Top 10** and **CWE**.

---

##  Methodology
The testing process followed a structured approach:

1. **Information Gathering** – Collected data on target systems and applications.
2. **Scanning & Enumeration** – Identified open ports, services, and accessible resources.
3. **Vulnerability Analysis** – Mapped potential weaknesses from gathered data.
4. **Exploitation** – Executed controlled attacks to verify vulnerabilities.
5. **Reporting** – Documented findings with technical details and business impact.
6. **Remediation** – Provided security improvement recommendations.

---

##  Risk Summary
| Risk Level | Count |
|------------|-------|
| Critical   | 2     |
| High       | 4     |
| Medium     | 2     |
| Low        | 2     |
| Informational | 0  |

---

##  Detailed Findings
| #  | Vulnerability | Target | Severity | CVSS | OWASP Top 10 |
|----|--------------|--------|----------|------|--------------|
| 1  | SQL Injection | DVWA | Critical | 9.8 | A03:2021 – Injection |
| 2  | Command Injection | DVWA | Critical | 9.8 | A03:2021 – Injection |
| 3  | File Upload (Web Shell) | DVWA | High | 8.6 | A08:2021 – Software & Data Integrity Failures |
| 4  | Information Disclosure via Help Icon | Zero Web App | High | 7.5 | A01:2021 – Broken Access Control |
| 5  | Insecure Direct Object Reference (IDOR) | Zero Web App | High | 7.7 | A01:2021 – Broken Access Control |
| 6  | Unprotected Admin Functionality | PortSwigger Lab | High | 7.7 | A01:2021 – Broken Access Control |
| 7  | Stored XSS in Transaction Description | Zero Web App | Medium | 6.1 | A07:2021 – XSS |
| 8  | Flawed Business Logic in Coupon Codes | PortSwigger Lab | Medium | 5.8 | A04:2021 – Insecure Design |
| 9  | Information Disclosure via Error Message | PortSwigger Lab | Low | 3.7 | A05:2021 – Security Misconfiguration |
| 10 | Directory Enumeration | Zero Web App | Low | 3.4 | A05:2021 – Security Misconfiguration |

---

##  Key Remediation Recommendations
- Implement **input validation** and **parameterized queries** to prevent injection attacks.
- Apply **strict access control** for sensitive endpoints and admin panels.
- Validate and sanitize **file uploads** with whitelist-based file type restrictions.
- Avoid exposing sensitive data in client-side code or verbose error messages.
- Regularly conduct **secure code reviews** and **automated vulnerability scans**.

---

##  Full Report
[ Download Full VAPT Report (PDF)](report.pdf)

The full report includes:
- Proof-of-concept exploitation steps
- Impact assessment
- Screenshot evidence
- Remediation steps for each vulnerability

---

##  Notes
- This assessment was conducted in a controlled lab environment.
- The purpose is purely educational and intended for security skill demonstration.

---
