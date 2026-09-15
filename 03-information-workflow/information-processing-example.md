# Information Processing Workflow Example

## Raw Input (Unstructured IT Helpdesk Tickets)
- "I can't generate the monthly sales report. It just spins for 5 minutes and then gives me a timeout error."
- "The new user registration page is throwing an ORA-00001 unique constraint error when I try to create an account."
- "Dashboard is incredibly slow today, taking forever to load the Q3 metrics."

## Chosen Task & Why
**Tasks Used:** Categorization and Extraction. 
**Why:** As a Systems Analyst, reading through unstructured user complaints is inefficient. I used AI to extract the technical symptoms, categorize the root database issues, and assign priority levels so the DBA team can tackle critical backend errors first.

## Prompt Used
"Act as a Systems Analyst. Read the raw helpdesk tickets. Extract the technical issue, map it to a potential database root cause, assign a priority level, and define an action item. Output as a Markdown table."

## AI Output & Final Structured Output (After Human Review)
*Note: Refined the AI draft to specify the exact database components (e.g., Indexing, Unique Constraints).*

| User Symptom | Database Root Cause | Priority | Action Item |
|---|---|---|---|
| Report generation timeout (5 mins) | Query performance / Missing Index | High | Analyze execution plan for the sales reporting query and create a composite index. |
| ORA-00001 on registration | Primary Key / Constraint Violation | Critical | Review the sequence generator for the Users table to prevent ID duplication. |
| Slow Q3 metrics dashboard | High CPU load / Lock Contention | Medium | Monitor active database sessions and identify blocking locks during peak hours. |
