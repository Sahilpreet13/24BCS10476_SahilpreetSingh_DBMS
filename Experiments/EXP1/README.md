# SQL Experiment 1 – Hospital Management Database

## 📌 Objective

The objective of this experiment is to practice SQL `INSERT` and `SELECT` statements by populating multiple related tables in a Hospital Management Database and retrieving records from them.

---

## 📖 Problem Statement

Insert the given data into the following tables exactly as specified:

- Doctors
- Patients
- Appointments
- Treatments
- MedicalRecords
- Billing

After inserting the data, retrieve the **first record** from the following tables:

- Doctors
- Patients
- Appointments

This experiment is based on the SQL Intermediate course available on CodeChef. :contentReference[oaicite:0]{index=0}

---

## 🗂 Database Tables

1. Doctors
2. Patients
3. Appointments
4. Treatments
5. MedicalRecords
6. Billing

---

## 🛠 SQL Concepts Used

- INSERT INTO
- SELECT
- WHERE clause
- Primary Keys
- Foreign Keys
- Relational Database Design

---

## 📄 Queries Performed

### Data Insertion

Inserted records into:

- Doctors
- Patients
- Appointments
- Treatments
- MedicalRecords
- Billing

### Data Retrieval

Retrieved the first record from:

```sql
SELECT * FROM Doctors WHERE DoctorID = 1;

SELECT * FROM Patients WHERE PatientID = 1;

SELECT * FROM Appointments WHERE AppointmentID = 1;
```

---

## ✅ Output

The queries successfully inserted all records and returned the first record from each of the following tables:

- Doctors
- Patients
- Appointments

---

## 📷 Sample Output

> Screenshot of successful execution:

![Output Screenshot](Screenshot%202026-07-13%20123923.png)

---

## 📁 Files

```
.
├── experiment.sql        # SQL queries
├── README.md             # Documentation
└── Screenshot 2026-07-13 123923.png
```

---

## 🎯 Learning Outcomes

After completing this experiment, I learned how to:

- Insert records into multiple related tables.
- Maintain relationships using foreign keys.
- Retrieve specific records using the `SELECT` statement.
- Work with a simple relational database schema.
- Execute and verify SQL queries successfully.

---

## 🚀 Platform

- **Course:** CodeChef SQL Intermediate
- **Language:** SQL
- **Database:** MySQL

---

## 👨‍💻 Author

**Sahilpreet Singh**

GitHub: https://github.com/Sahilpreet13
