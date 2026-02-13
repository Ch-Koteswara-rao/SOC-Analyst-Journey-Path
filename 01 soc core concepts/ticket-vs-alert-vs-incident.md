# Ticket vs Alert vs Incident

In SOC environments, alerts, tickets, and incidents represent different stages of threat detection and response. Each plays a specific role in identifying, tracking, and responding to potential security threats.

---

## 🚨 Alert

An alert is generated when a monitoring system detects activity that deviates from normal behavior. It serves as an indicator that something requires analyst attention.

Alerts are not automatically considered malicious. They must be reviewed to determine their relevance and risk.

Analyst actions:

- Examine the alert source and affected endpoint
- Review the process, file, or user activity involved
- Determine whether the behavior appears suspicious or expected

Example:

```
Alert: Unusual command execution detected
Endpoint: HR-PC-02
Status: Open
```

At this stage, the activity is flagged but not confirmed as a threat.

---

## 🎫 Ticket

A ticket is created to formally track the analysis and resolution of a security event. It ensures proper documentation and accountability throughout the investigation process.

Tickets help organize investigation workflow and maintain a record of findings.

Analyst actions:

- Open a ticket for alerts that require deeper analysis
- Record investigation observations and actions taken
- Update ticket status until resolution

Example:

```
Ticket ID: SOC-2026-014
Event: Suspicious executable detected
Status: Analysis ongoing
```

The ticket provides structured tracking of the investigation.

---

## 🔥 Incident

An incident is declared when analysis confirms unauthorized or malicious activity. This indicates that security has been compromised or a threat is actively present.

Incidents require immediate attention and response.

Analyst actions:

- Confirm indicators of compromise
- Escalate the case for containment and remediation
- Document confirmed malicious behavior

Example:

```
Incident: Unauthorized process execution confirmed
Impact: Malicious activity identified on endpoint
Status: Escalated
```

This represents a verified security threat.

---

## 🔄 Investigation Flow

The relationship between alert, ticket, and incident follows this sequence:

```
Alert → Ticket → Incident
```

- Alert identifies unusual activity
- Ticket tracks investigation and analysis
- Incident confirms malicious activity and triggers response

---

## Key Understanding

- Alerts indicate activity that requires review
- Tickets provide investigation tracking and documentation
- Incidents represent confirmed threats requiring response
