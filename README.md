# 🛡️ Nessus Vulnerability Scan - Localhost

## Objective
Perform a full vulnerability scan on the localhost using Nessus Essentials and summarize critical findings.

---

## Tools Used
- Nessus Essentials (Tenable)
- Localhost (127.0.0.1) as scan target
- Telnet Client (for firewall test)
- Windows 10

---

### Scan Summary
- Total high/critical vulnerabilities: 5

---

## Notable Vulnerabilities

### 1. TLS Version 1.0 Protocol Detection
- **Severity**: 3 (High/Critical)
- **Host**: 127.0.0.1
- **Port**: 3389/tcp
- **Description**: The remote service encrypts traffic using TLS 1.0. TLS 1.0 has known cryptographic flaws and is deprecated.
- **Suggested Fix**: Disable support for TLS 1.0 and use TLS 1.2 or higher.

### 2. SSL Certificate Cannot Be Trusted
- **Severity**: 3 (High/Critical)
- **Host**: 127.0.0.1
- **Port**: 8834/tcp
- **Description**: The X.509 certificate of the remote host cannot be trusted. This is often the case with self-signed certificates.
- **Suggested Fix**: Purchase or generate a certificate from a trusted certificate authority.

### 3. SSL Self-Signed Certificate
- **Severity**: 3 (High/Critical)
- **Host**: 127.0.0.1
- **Port**: 8834/tcp
- **Description**: The SSL certificate chain for this service ends in a self-signed certificate.
- **Suggested Fix**: Replace the self-signed certificate with one signed by a trusted certificate authority.

### 4. SSL Certificate With Wrong Hostname
- **Severity**: 3 (High/Critical)
- **Host**: 127.0.0.1
- **Port**: 8834/tcp
- **Description**: The SSL certificate used by this service was issued for a different hostname.
- **Suggested Fix**: Ensure that the certificate common name (CN) matches the hostname.

### 5. SSL Weak Cipher Suites Supported
- **Severity**: 3 (High/Critical)
- **Host**: 127.0.0.1
- **Port**: 8834/tcp
- **Description**: The remote service supports the use of SSL ciphers that offer either weak encryption or no encryption at all.
- **Suggested Fix**: Reconfigure the affected application to disable the weak ciphers.

---

## Outcome
Nessus successfully scanned the localhost system and identified key vulnerabilities. The findings can help guide patching and hardening actions to improve the system's security posture.
