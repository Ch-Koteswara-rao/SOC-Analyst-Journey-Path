# 🛡️ Lab 2: Junior Security Analyst Intro  
**SOC Analyst Journey Path | Practical Labs**

---

## 📌 Overview
This practical lab simulates **a day in the life of a Junior Security Analyst** working in a Security Operations Center (SOC).  
The lab focuses on monitoring alerts in a SIEM dashboard, identifying suspicious activity, and following proper escalation and response procedures.

🔗 **Room Link:**  
https://tryhackme.com/room/juniorsecurityanalystintro

---

## 🧪 Lab Details
In this lab, I interacted with a simulated **SIEM dashboard** :

- Reviewed the incoming security alerts
- Identified a malicious IP address
- Investigated login-related alerts
- Escalated the incident to the appropriate authority
- Applied a firewall action to block the IP

This lab reflects real SOC Level 1 analyst responsibilities.

---

## 🧾 Evidence Observed
The following evidence was identified from the SIEM alerts:

➤ Multiple unauthorized SSH login attempts  
➤ Successful SSH login from a suspicious external IP  
➤ Repeated failed login attempts to port 22  
➤ High-severity (Critical) alerts related to authentication abuse  

**Malicious IP Address Identified:**  
`221.181.185.159`

---

## 🔍 Analysis
The alert pattern indicated a **brute-force style SSH attack** followed by a successful login.  
The repeated failed attempts and the critical severity level confirmed that the activity was **malicious** and required immediate action.

Key indicators:
- External IP attempting multiple logins
- Critical alert severity
- Successful authentication after failed attempts

---

## 🚨 Decision Made
Based on the analysis:

➤ The alert was **escalated** to Level2 SOC analyst
➤ The malicious IP address was **blocked using the firewall**  
➤ The incident followed proper SOC escalation procedures  

**Escalated To:**  
Will Griffin

---

## ✅ Conclusion
The lab demonstrated how a Junior SOC Analyst:

- Identifies malicious behavior using SIEM alerts
- Makes informed decisions based on evidence
- Follows escalation procedures correctly
- Takes defensive action to protect systems

This reflects real-world SOC workflows and responsibilities.

---

## 🎯 Outcomes Learned
After completing this lab, I learned how to:

➤ Monitor and analyze SIEM alerts  
➤ Identify malicious IP addresses  
➤ Perform basic incident triage  
➤ Escalate security incidents properly  
➤ Apply firewall actions as part of incident response  

---

## 📈 Status
✔️ Lab Completed

---
