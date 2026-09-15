# Responsible AI & Governance Analysis

## Six Practical Concepts
- **Accuracy:** Validating AI-generated SQL execution plans against actual database performance metrics.
- **Accountability:** The DBA assumes full responsibility for any AI-generated code executed in the production environment.
- **Confidentiality:** Scrubbing all Personally Identifiable Information (PII) from data schemas before asking AI for optimization advice.
- **Privacy:** Ensuring that no real user records are used in prompts when generating test data.
- **Bias:** Designing database schemas and AI algorithms that do not inherently disadvantage specific user demographics.
- **Human Oversight:** Requiring peer review and explicit DBA sign-off before deploying any AI-suggested structural changes.

## Data Sensitivity Classification (Applied to Portfolio Content)
| Information Item Used in Portfolio | Classification | Reason |
|---|---|---|
| Database Schema Structures (Table Names, Columns) | Amber | Internal system architecture; anonymized for the prompt, but requires caution. |
| Actual Customer Records / Financial Transactions | Red | Highly confidential. NEVER included in any AI prompts or portfolio examples. |
| Generic Error Codes (e.g., ORA-00001) | Green | Standard, public software error codes safe for AI analysis. |
