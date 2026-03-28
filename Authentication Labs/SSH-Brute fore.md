# 🔐 Authentication Analysis  
### Brute Force & Successful Login Correlation

---

## 📌 Overview

This analysis focuses on identifying suspicious authentication behavior on a monitored Kali Linux endpoint using Wazuh SIEM.

The observed activity includes multiple failed login attempts followed by a successful authentication for the same user, indicating a potential credential compromise scenario.

---

## 🖥️ Environment

| Component | Details |
|----------|--------|
| SIEM | Wazuh |
| Endpoint | Kali Linux |
| Log Source | SSH (sshd) authentication logs |

---

## 🚨 Detection Summary

During monitoring, repeated authentication failures were observed targeting a valid user account.

Further correlation of events revealed that these failed attempts were followed by a successful login, indicating a transition from unauthorized access attempts to confirmed system access.

---

## 🔎 Activity Details

### 🔗 Log Correlation Query

   agent.name:kali AND sshd

This query was used to analyze all SSH authentication-related events in a single timeline.

---

## 📊 Observed Events

- Multiple `authentication failed` events  
- Detection of repeated password failures (`User missed the password more than one time`)  
- Successful authentication event (`authentication success`)  

---

## 🧾 Log Evidence

<img width="1907" height="255" alt="Screenshot 2026-03-28 115955" src="https://github.com/user-attachments/assets/3185a155-81ae-45d2-97bc-c735260a4fe3" />


---

## 🧠 Event Sequence

The reconstructed activity sequence:

This query was used to analyze all SSH authentication-related events in a single timeline.


---

## 🧪 Analysis

The observed pattern is consistent with a targeted authentication attack:

- Repeated password attempts were performed against a valid account  
- Authentication eventually succeeded  
- System access was obtained using valid credentials  

The presence of a successful authentication following multiple failures indicates a high likelihood of credential compromise.

---

## ⚖️ SOC Assessment

| Field | Value |
|------|------|
| Severity | High |
| Classification | True Positive |
| Action | Escalated to SOC L2 |

---

## 📍 Justification

The correlation between multiple authentication failures and a subsequent successful login confirms unauthorized access.

This pattern aligns with credential compromise scenarios and requires immediate investigation and response.

---

## 🧾 Conclusion

This activity demonstrates the importance of analyzing authentication logs in a correlated manner.

Rather than evaluating individual events in isolation, combining failed and successful login events provides clear visibility into attack progression and compromise.
