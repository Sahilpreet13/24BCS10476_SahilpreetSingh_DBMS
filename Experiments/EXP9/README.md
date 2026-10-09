# Experiment 9 — Salary Validation and Transaction Control

This folder contains the SQL scripts and screenshots for Experiment 9. The examples use PostgreSQL and PL/pgSQL to demonstrate a trigger that rejects an excessive salary increase and transaction control with a savepoint.

## Contents

- `Exp9.txt` — SQL for sections 9.1 and 9.2.
- `9.1.png` — Screenshot of the trigger rejecting a salary increase above 15%.
- `9.2.png` — Screenshot of the employee rows after the transaction and rollback.

## 9.1 — Enforce a maximum salary hike

The `check_salary_hike()` trigger function compares the new salary with the existing salary. An update is rejected when `NEW.salary` is greater than 115% of `OLD.salary`; PostgreSQL raises an exception and cancels that update. The trigger runs before updates to the `salary` column on `Salary_Hike`.

The script then demonstrates an allowed update to 44,000 and a rejected update to 90,000 for employee 1. These examples assume the starting salary makes 44,000 no more than 15% above the original value, while 90,000 exceeds the limit.

![PostgreSQL output showing the salary hike exception](9.1.png)

## 9.2 — Savepoint and rollback

The transaction increases employee 1's salary by 5,000, creates a savepoint, and then attempts to set employee 2's salary to a negative amount. `ROLLBACK TO SAVEPOINT salary_update` undoes changes made after the savepoint while retaining earlier work in the transaction. `COMMIT` saves the remaining changes, and the final `SELECT` displays the table.

The shown result contains employee 1 at 35,000, employee 2 at 40,000, and employee 3 at 50,000. The invalid post-savepoint update has been rolled back.

![Employee table after rollback to the savepoint](9.2.png)

## Run the script

1. Open `Exp9.txt` in a PostgreSQL client such as pgAdmin.
2. For section 9.1, ensure a `Salary_Hike` table exists with `emp_id` and `salary` columns, and that employee 1 has a starting salary. Run the function and trigger definitions before running the two sample updates. The second update is expected to raise an exception.
3. For section 9.2, ensure `tran_employees` exists with `emp_id` and `salary` columns and contains the employee rows used by the example. Run the transaction block, then inspect the final query result.

The script focuses on the trigger and transaction statements; it does not include table-creation or sample-data setup statements.
