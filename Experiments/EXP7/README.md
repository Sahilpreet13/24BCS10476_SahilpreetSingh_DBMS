# Experiment 7 — PL/SQL Explicit Cursor and Exception Handling

## Aim

To implement a PL/SQL program using an **explicit cursor** to retrieve employee details, increase the salary of employees by **10%**, and handle the condition where an employee has a salary of zero using a **user-defined exception**.

---

## Problem Statement

Write a PL/SQL program that:

1. Creates an explicit cursor to retrieve `EMP_ID` and `SALARY` from the `EMPLOYEE` table.
2. Fetches employee records one by one using the cursor.
3. Checks whether the employee's salary is zero.
4. If the salary is zero, raises a user-defined exception `SALARY_ZERO`.
5. If the salary is not zero, increases it by 10%.
6. Displays an appropriate message when the `SALARY_ZERO` exception occurs.

---

## Technologies Used

- Oracle SQL
- PL/SQL
- FreeSQL
- GitHub

---

## Concepts Used

### 1. Explicit Cursor

An **explicit cursor** is used when we want to process the result of a query one row at a time.

The cursor used in this experiment is:

```sql
CURSOR emp_cursor IS
    SELECT EMP_ID, SALARY FROM EMPLOYEE;
