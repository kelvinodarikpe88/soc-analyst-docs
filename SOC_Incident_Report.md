# 🛡️ SOC Analyst Incident Report

---

## 📋 Case Information

| Field              | Details                          |
|--------------------|----------------------------------|
| **Case ID**        | INC-2026-0042                    |
| **Date Opened**    | 2026-04-28                       |
| **Date Closed**    | 2026-04-28                       |
| **Analyst Name**   | Jane Doe                         |
| **Severity Level** | 🔴 Critical / 🟠 High / 🟡 Medium / 🟢 Low |
| **Status**         | ✅ Resolved                      |

---

## 🚨 Incident Summary

**Incident Title:** Phishing Email Leading to Credential Compromise  
**Affected System(s):** User Workstation — DESKTOP-HR04  
**Affected User(s):** john.smith@dizzbo.com  

**Brief Description:**  
A phishing email was received by a user in the HR department. The user clicked
a malicious link and entered their credentials on a spoofed login page.
Unauthorized access to the user's email account was detected shortly after.

---

## 🔍 Investigation Details

### Timeline of Events

| Time (UTC)  | Event Description                                      |
|-------------|--------------------------------------------------------|
| 08:12 AM    | Phishing email received by user                        |
| 08:35 AM    | User clicked malicious link                            |
| 08:37 AM    | Credentials submitted on fake login page               |
| 09:01 AM    | Suspicious login from IP 185.220.101.45 (Russia)       |
| 09:15 AM    | Alert triggered in SIEM (Microsoft Sentinel)           |
| 09:20 AM    | SOC Analyst assigned and investigation started         |

---

### Indicators of Compromise (IOCs)

| Type         | Value                          |
|--------------|--------------------------------|
| Malicious URL | `http://login-secure-verify[.]com` |
| Source IP    | `185.220.101.45`               |
| Email Sender | `noreply@micros0ft-support[.]net` |
| File Hash (if any) | `d41d8cd98f00b204e9800998ecf8427e` |

---

## 🛠️ Actions Taken

1. **Containment:**
   - Disabled compromised user account in Active Directory
   - Blocked malicious IP `185.220.101.45` in firewall
   - Blocked malicious URL in web proxy/DNS filter

2. **Eradication:**
   - Forced password reset for affected user
   - Enabled MFA on the account
   - Scanned workstation with EDR tool — no malware found

3. **Recovery:**
   - Re-enabled user account after password reset and MFA setup
   - Confirmed no further unauthorized access
   - Reviewed email inbox for any auto-forwarding rules — none found

4. **Communication:**
   - Notified IT Manager and HR Department Head
   - User briefed on phishing awareness

---

## 📊 Root Cause Analysis

**Root Cause:** User lack of phishing awareness training led to credential
submission on a spoofed website. No MFA was enabled on the account,
allowing the attacker to gain immediate access.

---

## ✅ Resolution Summary

**Resolution:** Credentials were reset, MFA enforced, and malicious
infrastructure blocked across all security controls. No data exfiltration
was confirmed. Case closed after 48-hour monitoring showed no re-infection.

**Lessons Learned:**
- MFA should be mandatory for all accounts
- Phishing simulation training to be scheduled company-wide
- SIEM alert threshold reviewed for faster detection

---

## 📁 Evidence & Attachments

- [ ] Email headers saved: `evidence/phishing_email_headers.txt`
- [ ] SIEM alert screenshot: `evidence/siem_alert_042826.png`
- [ ] Firewall block log: `evidence/fw_block_log.txt`

---

## 🔏 Sign-Off

| Role             | Name         | Date       |
|------------------|--------------|------------|
| SOC Analyst      | Kelvin Odarikpe     | 2026-04-28 |
| SOC Team Lead    | Mark Johnson | 2026-04-28 |

---
*Document Version: 1.0 | Classification: CONFIDENTIAL — Internal Use Only*
