# aetherpay-risk-register
Enterprise Risk Register &amp; Scoring Framework for AetherPay Inc. (NIST SP 800-30 / PCI-DSS v4.0).
# AetherPay Inc. Enterprise Risk Register & Scoring Framework

[![Framework: NIST SP 800-30](https://img.shields.io/badge/Framework-NIST%20SP%20800--30-blue)](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)
[![Compliance: SOC2 & PCI-DSS](https://img.shields.io/badge/Compliance-SOC2%20%7C%20PCI--DSS%20v4.0-green)](#)
[![Status: Production Ready](https://img.shields.io/badge/Status-Complete-brightgreen)](#)

## Executive Summary
This repository contains the operational **Enterprise Risk Management (ERM)** portfolio project for **AetherPay Inc.**, a hypothetical cloud-native FinTech organization processing over $500M annually in transaction volume across AWS cloud infrastructure.

As a Senior GRC Analyst, I designed and implemented this project to demonstrate end-to-end risk lifecycle management: establishing quantitative scoring thresholds, evaluating technical cloud risks, mapping control frameworks, and authoring executive briefs for leadership decision-making.

---

## 📁 Repository Architecture
---

## 🎯 Key Highlights & Deliverables

### 1. Risk Scoring Methodology (`docs/Risk_Assessment_Methodology.md`)
* Built upon **NIST SP 800-30 Rev. 1** and **FAIR** principles.
* Features a quantitative **$5 \times 5$ Likelihood vs. Impact matrix**.
* Establishes concrete financial impact thresholds (e.g., Impact 5 = $>\$1\text{M}$ financial loss or payment gateway suspension).
* Defines clear SLAs for remediation (High = 14–30 Days, Medium = 60 Days, Low = 90–180 Days).

### 2. Enterprise Risk Register (`templates_and_data/Risk_Register_Export.csv`)
Tracks 8 realistic technical and operational cloud risk scenarios, mapping each to **NIST SP 800-53**, **SOC 2**, **PCI-DSS**, and **ISO 27001**.

#### Top Highlighted Risks Summary Table:

| Risk ID | Category | Risk Scenario Summary | Inherent Risk | Existing Controls | Residual Risk | Treatment | Primary Control Mapping |
| :---: | :--- | :--- | :---: | :--- | :---: | :---: | :--- |
| **R-101** | IAM / Cloud | Hardcoded AWS production secrets in internal GitHub codebases | **20 (High)** | GitHub Secret Scanning active | **10 (Med)** | Mitigate | NIST IA-2 / PCI-DSS 8.2 |
| **R-102** | Data Protection | Unencrypted database backups stored in Amazon S3 buckets | **12 (Med)** | S3 Block Public Access enabled | **4 (Low)** | Mitigate | NIST SC-28 / PCI-DSS 3.4 |
| **R-103** | Availability | Single-region reliance on primary payment clearinghouse API | **12 (Med)** | Vendor SLA commitments | **9 (Med)** | Mitigate | NIST CP-2 / SOC 2 A1.2 |
| **R-106** | Vulnerability | Critical container CVEs unpatched past 30-day SLA | **16 (High)** | Monthly vulnerability scanning | **8 (Med)** | Mitigate | NIST RA-5 / PCI-DSS 6.3.1 |

### 3. Executive Decision Memo (`docs/Executive_Risk_Memo.md`)
A formal 1-page CISO decision memo for **Risk ID: R-101 (Hardcoded Secrets)**, presenting a business case for procuring an enterprise secrets manager ($18k budget) versus accepting residual risk.

---

## 🛠️ How to Use & Review This Repository
1. Read the **[Scoring Methodology](docs/Risk_Assessment_Methodology.md)** to understand how risk impact thresholds were calculated.
2. Review the **[Risk Register CSV](templates_and_data/Risk_Register_Export.csv)** to inspect control effectiveness evaluations and framework crosswalks.
3. Examine the **[Executive Decision Memo](docs/Executive_Risk_Memo.md)** for an example of executive-level GRC communication.
