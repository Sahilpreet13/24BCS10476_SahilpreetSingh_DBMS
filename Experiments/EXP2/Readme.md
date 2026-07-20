# SQL Set Operators Lab

This repository contains SQL experiments demonstrating the implementation of **SQL Set Operators**: `UNION`, `UNION ALL`, `INTERSECT`, and `EXCEPT`.

These experiments were performed as part of a Database Management Systems (DBMS) laboratory exercise to understand how SQL combines and compares data from multiple tables.

---

## 📚 Topics Covered

- UNION
- UNION ALL
- INTERSECT
- EXCEPT

---

## 📖 Experiment Overview

### Experiment 2.1 – UNION
Combines records from two tables while removing duplicate rows.

```sql
SELECT *
FROM Arts
UNION
SELECT *
FROM Science;
```

---

### Experiment 2.2 – UNION ALL

Combines records from two tables while preserving duplicate rows.

```sql
SELECT emp_name
FROM Employee
UNION ALL
SELECT emp_name
FROM pt_employee;
```

---

### Experiment 2.3 – INTERSECT

Returns only the records that are common to both tables.

```sql
SELECT f_name
FROM fruit
INTERSECT
SELECT inv_name
FROM inventory;
```

---

### Experiment 2.4 – EXCEPT

Returns records present in the first table but absent in the second table.

```sql
SELECT f_name
FROM fruit
EXCEPT
SELECT inv_name
FROM inventory;
```

---

## 📌 SQL Set Operators Comparison

| Operator | Removes Duplicates | Purpose |
|-----------|-------------------|---------|
| **UNION** | ✅ Yes | Combines unique records from both queries |
| **UNION ALL** | ❌ No | Combines all records including duplicates |
| **INTERSECT** | ✅ Yes | Returns common records from both queries |
| **EXCEPT** | ✅ Yes | Returns records present only in the first query |

---

## 🛠️ Concepts Learned

- Combining multiple result sets
- Eliminating duplicate records
- Preserving duplicate records
- Finding common data between tables
- Identifying missing records
- Writing efficient SQL queries using Set Operators

---

## 💻 Technologies Used

- SQL
- DBMS
- Relational Databases

---

## 📂 Repository Structure

```
SQL-Set-Operators/
│
├── README.md
├── 2.1.png
├── 2.2.png
├── 2.3.png
├── 2.4.png
└── exp2.txt
```

---

## 📸 Output

Screenshots of each experiment's output are included in the repository.

---

## 🎯 Learning Outcomes

After completing these experiments, you will be able to:

- Use SQL Set Operators effectively.
- Understand the difference between `UNION` and `UNION ALL`.
- Retrieve common records using `INTERSECT`.
- Find non-matching records using `EXCEPT`.
- Apply Set Operators in real-world database scenarios.

---

## 👨‍💻 Author

**Sahilpreet Singh**

GitHub: https://github.com/Sahilpreet13

---

⭐ If you found this repository helpful, consider giving it a star!
