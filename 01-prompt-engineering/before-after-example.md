# Before/After Prompt Improvement Example

- **Before (Weak Prompt):** "Fix this slow PL/SQL code."
- **Initial Result:** The AI provided generic advice about databases and rewrote the code using completely different logic that broke the existing system dependencies.
- **After (Improved C.A.R.E. Prompt):** "Context: This PL/SQL package processes daily reports but takes 10 minutes to execute. Action: Optimize the cursor loops without changing the core business logic. Role: Database Administrator. Expected Output: The optimized PL/SQL code with comments explaining the performance changes."
- **Improved Result:** The AI maintained the business logic, replaced slow row-by-row cursors with BULK COLLECT operations, and added clear explanatory comments.
- **What Improved:**
  - Specified the exact performance issue (10 minutes execution time).
  - Constrained the AI to *not* change business logic.
  - Required specific technical comments explaining the changes for human review.
