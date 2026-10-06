# Tasks: RiskLens Copilot

## Phase 1: Data and policy corpus
- [ ] Generate synthetic transactions, accounts, loans and LCR inputs
- [ ] Plant test patterns: structuring, LCR dip, SMA-1 cluster
- [ ] Collect policy, KYC and circular text; split into cited passages with IDs

## Phase 2: Signals
- [ ] AML rules: sub-threshold repeat cash deposits, KYC mismatch
- [ ] Liquidity: LCR vs regulatory and internal trigger, maturity look-ahead
- [ ] Credit: DPD buckets, SMA-1 movement, collateral cover

## Phase 3: Evidence and answers
- [ ] Natural-language to query for structured data
- [ ] Retrieval over policy text with source IDs
- [ ] Grounded finding with confidence and "no evidence" fallback

## Phase 4: Reports
- [ ] STR draft, ALCO note, credit memo templates
- [ ] Require citations for every section
- [ ] Human approval step

## Phase 5: Governance
- [ ] Roles: Compliance, Analyst, Auditor
- [ ] Masking of IDs and PII
- [ ] Audit log of query, sources, access level, approver

## Phase 6: UI and testing
- [ ] Signal, evidence, finding, report panels
- [ ] Test the three scenarios and the analyst restrictions
- [ ] Check regulatory thresholds and deadlines against current sources

## Phase 7: Submission
- [ ] Record 2-minute demo
- [ ] Final README review
- [ ] Judging check: relevance, technical execution, completeness
