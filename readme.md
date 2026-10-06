# RiskLens Copilot

An evidence-first copilot for banks and NBFCs. Ask a question in plain English, get a risk signal, the supporting data and policy text, a documented finding, and an audit-ready report draft.

## Why it matters
Fraud, liquidity and credit teams juggle transaction systems, policy documents and manual reports. RiskLens shortens the path from signal to filing while keeping every step traceable.

## Demo
Open `index.html` in a browser. Pick a role, then try:
- "Any structuring patterns this week?" (AML)
- "Is our LCR near the internal limit?" (liquidity, Basel)
- "Which loans show early credit deterioration?" (credit)

Switch to Business Analyst to see masking and report restriction. Use Approve and log to record human sign-off.

## How it works
1. Signal: detection rules flag unusual patterns with severity.
2. Evidence: matching rows plus retrieved policy and regulation passages, each cited.
3. Finding: a conclusion with confidence, drawn only from the evidence.
4. Report: an STR draft, ALCO note or credit memo, held for human approval.

## Architecture (target)
- Data layer: transactions, accounts, loans and liquidity tables in a governed warehouse.
- Retrieval: search over policies, KYC notes and circulars.
- Reasoning: LLM generates SQL and answers, constrained to retrieved evidence.
- Governance: role-based access, masking policies, query audit log.
- UI: single-page copilot with signal, evidence, finding and report panels.

## Governance and safety
- Reports cite sources and never include uncited claims.
- A person approves before a report is final.
- The copilot says when evidence is insufficient.

## Limits
The demo uses synthetic data and fixed scenarios. Thresholds and filing deadlines shown are examples; verify them against current RBI, FIU-IND and Basel text before real use.

## Files
index.html, requirements.md, readme.md, tasks.md
