# Requirements: RiskLens Copilot

## Problem
Banks and NBFCs handle real-time fraud, liquidity and credit risk plus regulatory reporting (AML, Basel, local rules) largely by hand. Analysts search transactions, then policy PDFs, then write reports. This is slow, hard to audit and easy to get wrong.

## Goal
A copilot that answers natural-language questions with governed, explainable, evidence-backed output, and carries each answer from signal to evidence to documented finding to report.

## Users
- Compliance officer / MLRO: investigates AML signals, approves STR drafts.
- Risk and treasury analyst: monitors liquidity and credit signals.
- Business user: asks questions with restricted, masked access.
- Auditor: reviews the trail of questions, sources and approvals.

## Functional requirements
1. FR1 Natural-language questions across fraud/AML, liquidity and credit risk.
2. FR2 Combine structured data (transactions, accounts, loans, LCR inputs) with unstructured text (policies, filings, KYC notes, circulars).
3. FR3 Signal view: severity, summary and trigger for each risk.
4. FR4 Evidence view: source rows plus cited policy or regulation passages, each with an ID.
5. FR5 Finding: plain-language conclusion with a confidence score and a recommended action.
6. FR6 Report draft (STR, ALCO note, credit memo) generated from the cited evidence only.
7. FR7 Human approval gate before anything is marked final.
8. FR8 Role-based access: field masking and report restriction by role.
9. FR9 Audit trail: query ID, role, sources used, access level, approver.
10. FR10 Refuse or say "no evidence found" when sources do not support an answer.

## Non-functional requirements
- Governance: role-based access, PII masking, no data leaves the governed platform.
- Explainability: every claim links to a row or passage.
- Accuracy: answers grounded in retrieved evidence; no uncited statements in reports.
- Performance: signal to report draft in under 15 seconds on sample data.
- Auditability: immutable log retained per bank policy.
- Compliance caution: thresholds and deadlines must be verified against current regulator text before production use.

## Data
| Source | Type | Examples |
|---|---|---|
| Transactions | Structured | cash deposits, transfers |
| Accounts / KYC | Structured + text | expected activity, occupation |
| Loans | Structured | DPD, exposure, collateral cover |
| Liquidity inputs | Structured | HQLA, net outflows |
| Policies and filings | Unstructured | AML, liquidity, credit policy; STR templates; regulator circulars |

All demo data is synthetic.

## Success criteria
- Three end-to-end scenarios (AML, liquidity, credit) work.
- Each report cites at least two sources.
- Analyst role never sees unmasked IDs or report drafts.
- Every query appears in the audit trail.

## Out of scope
Live regulator filing, real customer data, automated decisions without human approval.
