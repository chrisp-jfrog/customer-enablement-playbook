# Escalation & Incident Runbook

> **Purpose:** Define clear escalation paths, owners, and response SLAs so no customer issue falls through the cracks.
> **Owner:** Customer Success Management
> **Applies to:** All customer tiers during onboarding and post-launch

---

## Escalation Principles

1. **Escalate early, not late.** A premature escalation is always recoverable. A missed one rarely is.
2. **One owner per escalation.** Assign a single DRI (Directly Responsible Individual) for every open escalation.
3. **Customer communication within SLA.** The customer should never be the one chasing status.
4. **Document everything.** Log all escalations in the CRM with timestamps, owners, and resolution notes.

---

## Severity Levels

| Severity | Definition | Example |
|---|---|---|
| **SEV-1 — Critical** | Customer blocked; business impact; at-risk of churn | Product down, data loss, integration failure at go-live |
| **SEV-2 — High** | Major feature broken or adoption significantly impaired | SSO misconfiguration, key workflow failing for >50% of users |
| **SEV-3 — Medium** | Non-critical issue causing friction; workaround exists | Minor UI bug, delayed data sync, user permission issue |
| **SEV-4 — Low** | Cosmetic issue or question; no operational impact | Typo in email, how-to question, non-urgent feature request |

---

## Response SLAs

| Severity | First Response | Status Update Cadence | Target Resolution |
|---|---|---|---|
| SEV-1 | 30 minutes | Every 2 hours | 4 hours |
| SEV-2 | 2 hours | Every 4 hours | 1 business day |
| SEV-3 | 1 business day | Every 2 business days | 5 business days |
| SEV-4 | 2 business days | Weekly | 10 business days |

---

## Escalation Paths

### SEV-1 — Critical

```
CSM detects or receives report
      ↓
Immediately notify: CSM Manager + VP of CS (Slack + phone)
      ↓
Loop in: SE Lead + Support Engineering
      ↓
Open war room (Slack channel: #incident-[customer-name])
      ↓
Customer acknowledged within 30 min ← CSM owns this
      ↓
Engineering engaged if product issue confirmed
      ↓
Hourly internal updates until resolved
      ↓
Post-incident review within 48 hours
```

**DRI:** CSM Manager
**Customer Communication:** CSM
**Template:** [SEV-1 Acknowledgment](../guides/email-templates.md#sev-1-incident-acknowledgment)

---

### SEV-2 — High

```
CSM identifies issue
      ↓
Notify: CSM Manager (Slack, same business day)
      ↓
Engage: Support or SE depending on issue type
      ↓
Customer updated within 2 hours
      ↓
Daily internal standups until resolved
      ↓
Resolution confirmed with customer in writing
```

**DRI:** CSM
**Template:** [Issue Update](../guides/email-templates.md#issue-update)

---

### SEV-3 & SEV-4 — Medium / Low

```
CSM logs ticket in support system
      ↓
Tags: account name, severity, affected feature
      ↓
Customer acknowledged within SLA
      ↓
Tracked in weekly account health review
```

**DRI:** CSM
**Template:** [General Follow-Up](../guides/email-templates.md#general-follow-up)

---

## Onboarding-Specific Escalation Triggers

These scenarios during onboarding always require proactive escalation — do not wait for the customer to complain.

| Trigger | Severity | Escalate To |
|---|---|---|
| Kickoff not booked within 5 business days of signature | SEV-3 | CSM Manager |
| No admin login by Day 7 | SEV-2 | CSM Manager |
| Integration or SSO failure unresolved at Day 10 | SEV-1 | CSM Manager + SE Lead |
| Customer misses two consecutive scheduled calls | SEV-2 | CSM Manager + AE |
| Customer expresses dissatisfaction or asks about competitors | SEV-1 | CSM Manager + VP CS |
| No active users by Day 21 | SEV-2 | CSM Manager |

---

## CRM Logging Requirements

Every escalation must be logged in the CRM within 1 hour of detection. Required fields:

- **Account name and tier**
- **Severity level**
- **Date/time detected**
- **Issue description** (what is broken, what is the customer impact)
- **DRI name**
- **Current status**
- **Next action and due date**
- **Resolution date and root cause** (fill in at close)

---

## Post-Incident Review (SEV-1 & SEV-2)

Within 48 hours of a SEV-1 or SEV-2 resolution, the DRI must complete a post-incident review covering:

1. What happened and when
2. How it was detected
3. What actions were taken and by whom
4. Root cause (if known)
5. What we are doing to prevent recurrence
6. Customer sentiment post-resolution

Share the review with CSM Manager and VP CS. If the customer is enterprise tier, share a sanitized summary with their exec sponsor.

---

## Related Resources

- [Onboarding Checklist](../onboarding/customer-onboarding-checklist.md)
- [Email Templates](../guides/email-templates.md)

---

*Last updated: 2026-05-07 · Owner: Customer Enablement Team*
