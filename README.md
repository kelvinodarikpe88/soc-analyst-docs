# soc-analyst-docs
SOC Incident Reports and Case Logs
# SOC Analyst Documentation Hub

> Internal security operations documentation.  
> Classification: **CONFIDENTIAL — Internal Use Only**

---

## Repository Structure

```
soc-analyst-docs/
├── incidents/          # Incident reports and case logs
├── playbooks/          # Response procedures by threat type
├── ioc-tracker/        # Indicators of Compromise log
└── .github/            # Issue templates for new cases
```

---

## Quick Links

| Resource | Path |
|---|---|
| New Incident Template | `incidents/INC-TEMPLATE.md` |
| Phishing Playbook | `playbooks/phishing-playbook.md` |
| IOC Tracker | `ioc-tracker/ioc-log.md` |

---

## How to Log a New Incident

1. Copy `incidents/INC-TEMPLATE.md`
2. Create a new file: `incidents/INC-YYYY-NNNN.md`
3. Fill in all fields
4. Commit with message: `Add incident INC-YYYY-NNNN`
5. Open a GitHub Issue linked to this file

---

## Severity Levels

| Level | Label | Response Time |
|---|---|---|
| P1 | Critical | 15 minutes |
| P2 | High | 1 hour |
| P3 | Medium | 4 hours |
| P4 | Low | 24 hours |

---

## Team

| Role | Name | Contact |
|---|---|---|
| SOC Lead | Your Name | your.email@company.com |
| Analyst L1 | | |
| Analyst L2 | | |

---

*Last updated: 2026-04-28 | Version: 1.0*
