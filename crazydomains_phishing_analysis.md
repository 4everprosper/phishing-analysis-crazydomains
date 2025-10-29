# 🧠 Phishing Analysis Report — sitebeat.crazydomains.com

**Author:** Chris Gibson  
**Date:** October 22, 2025  
**Classification:** ⚠️ *Malicious — Phishing / Credential Harvesting*  

---

## 1. Executive Summary
This investigation analyzes the domain `sp910846.sitebeat.crazydomains.com`, identified as **malicious** and associated with **phishing activity**.  
The domain leverages a legitimate web hosting provider (**CrazyDomains Sitebeat**) to host a cloned login page intended to harvest credentials.

This is an example of **abuse of legitimate infrastructure**, where attackers host phishing content on trusted domains to evade detection.

---

## 2. Technical Analysis

| Attribute | Detail |
|------------|---------|
| **Full URL** | `https://sp910846.sitebeat.crazydomains.com/` |
| **Root Domain** | `crazydomains.com` *(legitimate)* |
| **Subdomain** | `sp910846.sitebeat` *(malicious)* |
| **Hosting Provider** | CrazyDomains / Sitebeat Web Builder |
| **SSL Certificate** | Valid (Let’s Encrypt) |
| **Observed Behavior** | Cloned login form collecting credentials |

### 🔸 Observations
- Page impersonates a legitimate login page.
- SSL used to appear trustworthy.
- POST requests sent to unknown PHP endpoint.
- Likely distributed via phishing email or SMS.

---

## 3. Threat Assessment

| Category | Value |
|-----------|--------|
| **Threat Type** | Phishing / Credential Harvesting |
| **TTPs (MITRE ATT&CK)** | `T1566.002 – Spearphishing Link`, `T1056 – Input Capture` |
| **Risk Level** | 🟥 High |

---

## 4. Indicators of Compromise (IOCs)

| Type | Value |
|------|--------|
| URL | `https://sp910846.sitebeat.crazydomains.com/` |
| Hostname | `sp910846.sitebeat.crazydomains.com` |
| Registrar | CrazyDomains Pty Ltd |
| SSL Issuer | Let’s Encrypt |

---

## 5. Mitigation Recommendations
- **Block** the domain and subdomain in firewalls, DNS, and email filters.  
- **Report** to the hosting provider for takedown.  
- **Educate users** to verify URLs before entering credentials.  
- **Monitor** for similar subdomains under `*.sitebeat.crazydomains.com`.  
- **Add IOCs** to SIEM and threat intelligence watchlists.  

---

## 6. Conclusion
The domain is confirmed as **malicious**, hosting phishing content under a legitimate service provider.  
This demonstrates a common phishing tactic: using reputable infrastructure to deceive users and evade detection.

This project highlights:
- OSINT investigation
- IOC extraction
- Threat classification and mitigation
- Professional reporting and documentation

---

## 7. Resume Description
**Phishing Analysis Project — CrazyDomains Phish Investigation**  
Conducted a phishing investigation of a malicious subdomain hosted on a legitimate web platform.  
Identified malicious behavior, extracted IOCs, mapped MITRE ATT&CK techniques, and created mitigation recommendations.  
**Tools:** VirusTotal, URLScan.io, Whois Lookup, PhishTank.
