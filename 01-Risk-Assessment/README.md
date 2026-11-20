# 01 – Risk Assessment & Risk Register

**Scenario:** As the first Junior GRC Analyst at MapleCloud Technologies Inc. (fictional SaaS company, Fredericton, NB), I identified, scored and prioritized the company's top cybersecurity risks ahead of a SOC 2 audit.

> Simulation using fictional data. Not a real company or audit.

📄 **Files:**
- [MapleCloud_GRC_Company_Profile.docx](MapleCloud_GRC_Company_Profile.docx) – full company profile: operations, asset inventory, threats, roles, objectives, laws
- [MapleCloud-Risk-Register.csv](MapleCloud-Risk-Register.csv) – full risk register (15 risks)

## Company context

| | |
|---|---|
| Business | Cloud invoicing and scheduling app for small businesses |
| Size | 71 employees, ~1,200 business customers across Canada (incl. Quebec) |
| Systems | AWS (Canada region), Microsoft 365, GitHub, Stripe, Salesforce |
| Why now | Largest prospect, a regional credit union, requires a SOC 2 report and an SBOM before signing |
| Starting point | No security team, one policy, MFA not on all accounts, untested backups, some unencrypted laptops |
| Laws and standards | PIPEDA, Quebec Law 25, SOC 2, PCI DSS (via Stripe); ISO 27001 possible later |

## Method

- Built from the asset inventory and threats in the company profile
- Each risk = **threat + vulnerability + business impact**
- Scored on a 5×5 matrix: **Risk score = Likelihood × Impact** (1–25)
  - 🟢 Low 1–6 · 🟡 Medium 8–12 · 🔴 High 15–25
- **Inherent risk** = score today. **Residual risk** = expected score after the planned treatment.
- Each risk has an owner, treatment, target date and current controls

## Results

| Rating | Inherent (today) | Residual (after treatment) |
|---|---|---|
| 🔴 High | 8 | 0 |
| 🟡 Medium | 6 | 4 |
| 🟢 Low | 1 | 11 |
| **Total** | **15** | **15** |

## Treatment decisions

| Treatment | Risks | Why |
|---|---|---|
| Mitigate | 13 | Add or fix controls to lower the risk |
| Accept | 2 (R-07, R-12) | The fix costs more than the likely loss at MapleCloud's size; CEO signs off and the risk is reviewed yearly |
| Transfer (partial) | R-01, R-13 | Cyber insurance covers part of the financial loss, alongside the controls |

## Top 5 risks

| ID | Risk | Score | Owner | Treatment |
|---|---|---|---|---|
| R-06 | SOC 2 / compliance failure | 20 | Junior GRC Analyst | Write and approve core security policies |
| R-11 | Too many AWS admins | 20 | CTO | Role-based AWS permissions; quarterly reviews |
| R-02 | Phishing / stolen passwords | 16 | IT Manager | MFA for all accounts; security training |
| R-05 | Excessive access (no least privilege) | 16 | CTO | Role-based access control |
| R-15 | No security logging | 16 | IT Manager and CTO | Turn on CloudTrail and M365 audit logs; alerts |

## Key findings

1. **Access control is the biggest theme.** 5 of 15 risks come from too much access, missing MFA or no offboarding.
2. **Cloud security needs attention.** 4 risks are in AWS (open ports, root account, admin rights, single region).
3. **No policies, plans or monitoring.** Missing policies, no incident response plan and no logging would likely fail a SOC 2 audit.
