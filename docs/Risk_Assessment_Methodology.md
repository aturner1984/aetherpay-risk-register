# Enterprise Risk Assessment & Scoring Methodology
**Organization:** AetherPay Inc.  
**Version:** 2.0  
**Effective Date:** October 2026  
**Owner:** Governance, Risk, and Compliance (GRC) Team  

---

## 1. Overview & Purpose
AetherPay Inc. operates a cloud-native payment gateway processing over $500M in annual transactional volume across AWS cloud infrastructure. The purpose of this methodology is to establish a standardized, repeatable framework for identifying, quantifying, evaluating, and managing information security and operational risks across the enterprise.

This methodology aligns with **NIST SP 800-30 Rev. 1** (*Conducting Risk Assessments*), **ISO 27005**, and the **FAIR** (Factor Analysis of Information Risk) framework.

---

## 2. Risk Scoring Scales ($5 \times 5$ Matrix)

Risk is evaluated quantitatively and qualitatively using two parameters:
$$\text{Inherent Risk Score} = \text{Likelihood Rating} \times \text{Impact Rating}$$

### 2.1 Likelihood Scale (1–5)

| Rating | Level | Definition & Frequency | Probability |
| :---: | :--- | :--- | :---: |
| **1** | **Rare** | Expected to occur only in exceptional circumstances (>3 years). | $<10\%$ |
| **2** | **Unlikely** | May occur at some time (1–3 years). | $10\% - 30\%$ |
| **3** | **Possible** | Might occur within the next 12 months. | $31\% - 60\%$ |
| **4** | **Likely** | Likely to occur multiple times per year. | $61\% - 90\%$ |
| **5** | **Almost Certain** | Expected to occur frequently or continuously ($<1$ month). | $>90\%$ |

---

### 2.2 Impact Scale (1–5)

Impact criteria evaluate financial loss, operational downtime, legal/regulatory liability, and reputational damage. The highest rating across any single column determines the final score.

| Rating | Level | Financial Loss | Downtime / Operational | Regulatory & Compliance | Reputational |
| :---: | :--- | :--- | :--- | :--- | :--- |
| **1** | **Negligible** | $<\$10,000$ | None or minimal internal latency. | No regulatory impact. | No external visibility. |
| **2** | **Minor** | $\$10,000 - \$50,000$ | Internal disruption ($<1$ hour). | Minor non-conformity; no fines. | Limited local/industry awareness. |
| **3** | **Moderate** | $\$50,000 - \$250,000$ | Customer-facing outage ($1-4$ hours). | Regulatory reporting triggered; minor fine. | Social media attention; customer churn $<2\%$. |
| **4** | **Major** | $\$250,000 - \$1,000,000$ | Core payment gateway down ($4-12$ hours). | PCI-DSS non-compliance fine; formal audit finding. | National coverage; customer churn $2\%-10\%$. |
| **5** | **Critical** | $>\$1,000,000$ | Complete blackout ($>12$ hours). | Payment processing license suspension; HIPAA/GDPR class action. | Major news coverage; executive resignation; churn $>10\%$. |

---

## 3. Risk Thresholds & Action Matrix

Calculated Risk Scores range from **1 to 25**.

IMPACT
      1     2     3     4     5
   +-----+-----+-----+-----+-----+
 5 |  5  | 10  | 15  | 20  | 25  |

 | Risk Score | Level | Required Action & Escalation Path | Remediation SLA |
| :---: | :---: | :--- | :---: |
| **15 – 25** | **HIGH** | Immediate escalation to CISO & VP of Engineering. Requires formal mitigation project or explicit CISO Risk Acceptance Memo. | **14–30 Days** |
| **8 – 12** | **MEDIUM** | Assign risk owner. Implement compensating controls or schedule remediation into engineering sprint. | **60 Days** |
| **1 – 6** | **LOW** | Accept risk or manage via standard operational procedures and routine control monitoring. | **90–180 Days** |

---

## 4. Control Effectiveness Ratings

When calculating **Residual Risk** ($\text{Residual Risk} = \text{Inherent Risk} - \text{Control Mitigations}$), existing internal controls are evaluated as follows:

* **Effective (75%-100% Risk Reduction):** Control is automated, continuously tested, documented, and enforced without exceptions.
* **Partially Effective (25%-74% Risk Reduction):** Control is manual or decentralized, occasionally bypassed, or lacks automated logging/alerts.
* **Ineffective (0%-24% Risk Reduction):** Control is undocumented, unmonitored, or consistently fails during audit testing.

---

## 5. Control Mapping References
Every risk scenario logged in the Enterprise Risk Register must map to at least one primary control framework requirement:
* **NIST SP 800-53 Rev. 5**
* **SOC 2 Trust Services Criteria (2017)**
* **PCI-DSS v4.0**
* **ISO/IEC 27001:2022 Annex A**
