# 🎯 False Positive vs True Positive

During alert investigation, the primary task is to determine whether the detected activity represents a real security threat or normal system behavior. This classification determines whether escalation is required.

---

## ✅ True Positive

A True Positive means the alert correctly identified malicious activity. Investigation confirms that the process, file, or network activity is associated with a threat.

Analyst actions:

- Review the process execution and origin
- Check associated file, IP address, or domain reputation
- Identify indicators linked to known malicious activity
- Confirm abnormal or unauthorized behavior

Example:

```
Process: powershell.exe
Parent Process: winword.exe
Activity: External connection to malicious IP
```

This indicates malicious execution and requires escalation.

---

## ⚠️ False Positive

A False Positive means the alert was triggered, but the activity is legitimate and does not indicate a threat.

Analyst actions:

- Verify the process is expected and legitimate
- Confirm the activity matches normal user or system behavior
- Ensure no malicious indicators are present

Example:

```
Process: chrome.exe
Activity: User accessed external website
Observation: Normal browsing activity
```

This does not require escalation.

---

## 🧠 Key Understanding

- True Positive → Malicious activity confirmed → Escalation required
- False Positive → Legitimate activity confirmed → No escalation required
- Proper classification ensures accurate incident response
