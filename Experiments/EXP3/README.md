# Experiment 3 – SQL Aggregate Functions, Conditional Counting & Subqueries

## Aim

To understand and implement SQL aggregate functions, conditional counting using the `CASE` statement, grouping of records, filtering grouped data using the `HAVING` clause, and subqueries to retrieve meaningful information from relational databases.

---

## Objectives

- Learn the use of SQL Aggregate Functions such as `COUNT()`, `SUM()`, and `AVG()`.
- Understand conditional aggregation using the `CASE` statement.
- Apply the `GROUP BY` clause to categorize data.
- Use the `HAVING` clause to filter grouped results.
- Retrieve distinct values using the `DISTINCT` keyword.
- Implement subqueries to solve real-world SQL problems.
- Develop efficient SQL queries for data analysis and reporting.

---

# Exercise 3.1 – Count Using CASE

## Problem Statement

Write an SQL query to count the number of students in each department who have scored more than **80 marks**. Display the count using the alias **Dept_HighScore_Count**.

## Concepts Used

- `COUNT()`
- `CASE`
- `GROUP BY`

## SQL Query

```sql
SELECT Department,
COUNT(CASE WHEN Marks > 80 THEN 1 ELSE NULL END) AS Dept_HighScore_Count
FROM student
GROUP BY Department;
```

## Output

![Exercise 3.1 Output](3.1.png)

---

# Exercise 3.2 – Aggregate Functions on Employee Data

## Problem Statement

Create an **Employees** table and perform various analytical operations using SQL Aggregate Functions and grouping techniques.

## Tasks Performed

### 1. Count the number of employees in each city.

### 2. Count the number of employees in each city and sort the results:
- Ascending order of employee count.
- Descending order of employee count (if counts are equal, sort by city name).

### 3. Count employees having a salary greater than or equal to **90,000** in each city using conditional aggregation.

### 4. Use the `HAVING` clause to filter grouped data.

### 5. Calculate the average salary of employees in each city.

### 6. Display all distinct employee cities.

### 7. Count the total number of distinct cities.

## Concepts Used

- `COUNT()`
- `SUM()`
- `AVG()`
- `CASE`
- `GROUP BY`
- `HAVING`
- `ORDER BY`
- `DISTINCT`

## SQL Script

The complete SQL script for this exercise is available in **exp3.txt**. :contentReference[oaicite:0]{index=0}

---

# Exercise 3.3 – Customers Who Never Order

## Problem Statement

Retrieve the names of customers who have never placed an order using a subquery.

**Reference:** https://leetcode.com/problems/customers-who-never-order/

## Concepts Used

- Subqueries
- `NOT IN`
- Data Filtering

## SQL Query

```sql
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (
    SELECT customerId
    FROM Orders
);
```

## Output

![Exercise 3.3 Output](3.3.png)

---

# References

### Exercise 2.1

**CodeChef – SQL Intermediate**

https://www.codechef.com/learn/course/sql-intermediate/SQ00BS08/problems/GSQ82

### Exercise 2.3

**LeetCode 183 – Customers Who Never Order**

https://leetcode.com/problems/customers-who-never-order/

---

# Learning Outcomes

After completing this experiment, the following concepts were successfully implemented:

- SQL Aggregate Functions (`COUNT`, `SUM`, `AVG`)
- Conditional Aggregation using `CASE`
- Data Grouping with `GROUP BY`
- Filtering Groups using `HAVING`
- Sorting Results using `ORDER BY`
- Eliminating Duplicate Values using `DISTINCT`
- Writing Nested Queries (Subqueries)
- Solving real-world SQL problems using analytical queries
