# 🔐 Cybersecurity & Ethical Hacking Internship — Task 3
## Web Application Security Testing

**Internship Organization:** ApexPlanet Software Pvt. Ltd.  
**Task:** 3 — Web Application Security  
**Domain:** Cybersecurity & Ethical Hacking

---

## 📌 Objective

The objective of this task was to understand web application security testing by identifying and demonstrating common web vulnerabilities in a controlled lab environment using DVWA, Burp Suite, and OWASP ZAP.

## 🛠️ Tools & Technologies Used

- **Kali Linux** — Security testing environment
- **DVWA (Damn Vulnerable Web Application)** — Vulnerable web application for practical testing
- **Docker** — Running DVWA locally
- **Burp Suite Community Edition** — HTTP traffic inspection and proxy testing
- **OWASP ZAP 2.17.0** — Automated web application security scanning
- **Mozilla Firefox** — Accessing and testing the web application

## 💻 Lab Environment

| Component | Configuration |
|---|---|
| Operating System | Kali Linux |
| Virtualization | VMware |
| Vulnerable Application | DVWA |
| Application URL | `http://127.0.0.1:8080` |
| DVWA Security Level | Low |
| Burp Proxy Port | 8081 |
| OWASP ZAP Proxy Port | 8082 |

All testing was performed against the locally hosted DVWA application.

## 🔍 Practical Activities Performed

### 1. DVWA Setup and Configuration

- Installed and configured Docker in Kali Linux.
- Downloaded and launched the DVWA Docker container.
- Accessed DVWA through Firefox.
- Initialized the DVWA database.
- Logged in using the default lab credentials.
- Configured the security level to Low for vulnerability demonstrations.

### 2. SQL Injection Testing

- Opened the SQL Injection module in DVWA.
- Tested the following input:

```text
1' OR '1'='1
```

- Observed multiple user records being returned.
- Understood how unsafe SQL query construction can expose database information.

### 3. Burp Suite — HTTP Traffic Inspection

- Opened Burp Suite Community Edition.
- Configured the proxy listener on port 8081.
- Configured browser proxy settings.
- Used the Burp browser to access the local DVWA application.
- Worked with HTTP request inspection through the Proxy and HTTP History features.

### 4. OWASP ZAP — Automated Security Scanning

- Opened OWASP ZAP 2.17.0.
- Configured the local proxy on port 8082 to avoid a port conflict.
- Performed an automated scan against:

```text
http://127.0.0.1:8080
```

- Reviewed the Alerts panel.
- Observed 11 security alerts during the scan.

**Examples of observed security findings:**

- Content Security Policy (CSP) Header Not Set
- Directory Browsing
- Missing Anti-clickjacking Header
- Cookie Without SameSite Attribute
- Server Information Disclosure

### 5. Reflected Cross-Site Scripting (XSS)

- Opened the Reflected XSS module in DVWA.
- Tested a JavaScript payload:

```html
<script>alert('XSSVulnerability')</script>
```

- Observed a JavaScript alert popup in the browser.
- Confirmed that the application executed the injected JavaScript.

## 📸 Screenshots / Practical Evidence

The following screenshots document the practical activities:

<img width="1671" height="921" alt="Screenshot 2026-11-10 150646" src="https://github.com/user-attachments/assets/aa8b5271-e232-4cb3-a2b2-f818a113ab01" />

| SS 3.1 | DVWA Dashboard and Security Configuration |

<img width="1672" height="919" alt="Screenshot 2026-11-10 150811" src="https://github.com/user-attachments/assets/f12a5cfa-3bc9-4aed-8749-bf86a756e82f" />

| SS 3.2 | Burp Suite HTTP History and Request Inspection |

<img width="1671" height="909" alt="Screenshot 2026-11-10 150606" src="https://github.com/user-attachments/assets/82f43dba-3363-4f98-a75b-db4d2d2de839" />

| SS 3.3 | OWASP ZAP Automated Scan and Security Alerts |

<img width="1666" height="921" alt="Screenshot 2026-11-10 150422" src="https://github.com/user-attachments/assets/91717cc1-387b-4efc-bd6d-c7d53434a1be" />

| SS 3.4 | Reflected XSS JavaScript Alert Demonstration |


## 📊 Results

- Successfully configured and accessed DVWA locally.
- Demonstrated SQL Injection using a test input.
- Configured Burp Suite for HTTP traffic inspection.
- Completed an OWASP ZAP automated scan and observed 11 alerts.
- Successfully demonstrated Reflected XSS using a JavaScript alert payload.
- Understood common web application security weaknesses and the importance of secure input handling.

## 🎯 Learning Outcomes

Through this task, I gained practical knowledge of:

- Web application security testing.
- SQL Injection vulnerabilities.
- Reflected Cross-Site Scripting (XSS).
- HTTP request inspection using Burp Suite.
- Automated vulnerability scanning using OWASP ZAP.
- Identifying security misconfigurations.
- Understanding the importance of input validation and secure coding practices.

## 📝 Conclusion

Task 3 provided practical exposure to web application security testing in a controlled environment. By using DVWA, Burp Suite, and OWASP ZAP, I explored common web vulnerabilities, inspected HTTP traffic, and identified security-related issues through automated scanning. This task improved my understanding of web application vulnerabilities and basic penetration testing techniques.

## ⚠️ Ethical Disclaimer

All security testing was performed on a locally hosted DVWA application for educational purposes. No real-world websites or unauthorized systems were targeted.

---

**Cybersecurity & Ethical Hacking Internship — ApexPlanet Software Pvt. Ltd.**
