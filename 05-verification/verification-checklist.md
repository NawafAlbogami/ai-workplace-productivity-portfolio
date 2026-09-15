# Verification Checklist & Application

## Personal Verification Checklist
1. Verify SQL syntax against the specific database engine (e.g., Oracle vs SQL Server).
2. Ensure no destructive commands (DROP, DELETE without WHERE, TRUNCATE) are hallucinated by the AI.
3. Check execution logic and performance implications (e.g., avoiding full table scans).
4. Remove any hardcoded proprietary data from the prompt before generating code.
5. Test the AI-generated script in a safe Staging/Dev environment before Production.

## Applied Example
**Output Verified:** An AI-generated PL/SQL script intended to update customer statuses in bulk.
**Application Steps:**
- **Criteria 2 (No Destructive Commands):** I reviewed the AI script and found it lacked a `COMMIT` limit, which could lock the entire table. I manually added a batch processing limit (`LIMIT 1000`).
- **Criteria 3 (Performance):** The AI suggested using a standard `FOR` loop. I verified this was inefficient for large datasets and updated it to use `FORALL` (Bulk Bind) for better performance.
- **Criteria 5 (Testing):** Executed the verified script in the Dev database and confirmed it updated the 5,000 records successfully in under 2 seconds.
