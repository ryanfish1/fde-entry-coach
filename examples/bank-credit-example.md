# Example — Bank Credit Manager → Domain / Internal FDE

> This example is illustrative. Do not claim the numbers below as real project results unless you have actually measured them.

## Background

User profile:

- 5+ years in SME credit / corporate lending
- strong understanding of financial statements, customer materials, credit review, and approval workflows
- can use spreadsheets and AI coding tools, but is not a production software engineer

Recommended lane:

**Primary: Domain FDE**  
**Secondary: Internal FDE**

Reason: the strongest edge is understanding which customer documents matter, which exceptions require judgment, and where credit teams lose time.

## Bad project framing

> “Build an AI Agent for banking.”

Too broad. No user, no workflow, no metric.

## Narrowed project

> Build an AI-assisted pre-review workflow that extracts, cross-checks, and structures SME customer materials before a credit manager starts manual analysis.

## PSF

### Pain — 4/5

Credit managers repeatedly collect and reorganize business licenses, bank statements, financial statements, shareholder information, contracts, and internal notes.

### Economics — 4/5

If the process is frequent, reducing preparation time increases reviewer throughput and frees experienced staff for judgment-heavy work.

### Feasibility — 3/5

A personal project may have limited access to real bank systems and confidential data. Start with properly authorized, de-identified, or synthetic-but-realistic document structures, and seek a real user for workflow testing without exposing sensitive customer data.

**Total: 11/15**

Conclusion: viable after narrowing scope and solving data-access/privacy constraints.

## Minimum Five Maps

### Data

- business registration information
- financial statements
- transaction summaries
- shareholder / ownership structure
- loan application materials

Constraint: confidential financial and personal data must not be copied into unauthorized tools.

### Workflow

1. receive customer material
2. check completeness
3. manually locate key fields
4. compare across documents
5. flag inconsistencies
6. draft structured pre-review notes
7. begin judgment-heavy credit analysis

### Organization

- user: credit manager
- potential champion: team lead / experienced reviewer
- veto / constraint: risk, compliance, information-security teams

### System

For a first portfolio project, avoid pretending to integrate with a bank core system. Build a local or approved test environment that proves the workflow logic.

### Politics

Position the system as removing document preparation and reconciliation work, not replacing credit judgment or approval accountability.

## MVD

- **User:** SME credit manager
- **Workflow:** document intake → completeness check → key-field extraction → inconsistency flags → structured pre-review memo
- **Data:** authorized de-identified sample documents
- **Metric:** preparation time per case
- **Quality threshold:** critical fields require high recall; human review remains mandatory before any credit decision
- **Deadline:** 2–3 weeks
- **Graduation:** continue only if test users report meaningful time savings and no unacceptable critical omissions

## 30-day portfolio goal

Do not claim “AI replaces credit review.”

A credible case-study headline is closer to:

> Designed and tested an AI-assisted SME credit pre-review workflow that reduced repetitive document preparation while preserving human approval and risk review.

Collect real metrics before inserting a percentage or time reduction.
