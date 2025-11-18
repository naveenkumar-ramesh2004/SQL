# Day 01 — SQL Fundamentals (Extended)
---

## 1️⃣ What is SQL?
**SQL (Structured Query Language)** is a language used to talk to a database.
It allows you to store, read, update, and delete data.

Example:
```sql
SELECT * FROM students;
```
This gets all data from the `students` table.

---

## 2️⃣ Why SQL?
Because almost every application in the world needs to store data.
Apps like:
- Swiggy (restaurants, menu, orders)
- Amazon (products, users, payments)
- Instagram (posts, comments, followers)

They all use a database, and SQL is the language to manage that data.

---

## 3️⃣ Types of SQL
SQL commands are grouped into categories:

### ✔ DDL — Data Definition Language
Used to **define** or **change** structure of tables.
Examples:
- `CREATE`
- `ALTER`
- `DROP`
- `TRUNCATE`

### ✔ DML — Data Manipulation Language
Used to **manipulate** data.
Examples:
- `INSERT`
- `UPDATE`
- `DELETE`

### ✔ DQL — Data Query Language
Used to **fetch data**.
Example:
- `SELECT`

### ✔ DCL — Data Control Language
Used to give/remove permissions.
Examples:
- `GRANT`
- `REVOKE`

### ✔ TCL — Transaction Control Language
Used to manage transactions.
Examples:
- `COMMIT`
- `ROLLBACK`
- `SAVEPOINT`

---

## 4️⃣ Any difference between them?
Yes — each type has different purpose.
- DDL → structure
- DML → data
- DQL → read
- DCL → permissions
- TCL → transaction safety

---

## 5️⃣ What should a Full‑Stack Developer know?
As a React + Java Full Stack Developer, you must know:
- SQL basics (SELECT, INSERT, UPDATE, DELETE)
- Joins
- Primary key, foreign key
- Index
- Transactions
- Normalization
- MySQL installation & workbench
- JDBC (Java → SQL connection)
- JPA/Hibernate basics
- Query writing for backend APIs

---

## 6️⃣ How to Communicate with Database (JDBC)
Your Java code communicates with SQL database using **JDBC**.

Example flow:
1. Java program sends SQL query to DB
2. Database executes query
3. Sends results back to Java

---

## 7️⃣ What is JDBC? Why?
**JDBC (Java Database Connectivity)** is a Java API that helps Java programs talk to databases.

Why?
- SQL cannot directly talk to Java
- JDBC acts as a bridge
- You can run SQL queries inside Java

---

## 8️⃣ What is an API?
**API (Application Programming Interface)** allows communication between two applications.

Example:
React → API → Java Backend → MySQL

When you click “Order” in Soru Vandi:
- React calls API
- API writes order into database

---

## 9️⃣ Why API?
Because frontend cannot talk directly to database (security issue).
API acts as a **middle layer**.

---

## 🔟 Difference: File System vs Database
| File System | Database |
|------------|----------|
| Stores data in files | Stores data in tables |
| No relationships | Supports relationships (FK) |
| Slow search | Fast search (Index) |
| Not secure | Highly secure |
| No transactions | Supports ACID |

---

## 1️⃣1️⃣ DOC, DML, DCL, TCL
*(Already explained above)*

---

## 1️⃣2️⃣ What is Jupyter Notebook? Why?
Jupyter Notebook is an interactive environment used mainly for:
- Writing code
- Testing SQL
- Running Python + SQL together
- Data analysis

You can run SQL queries inside notebook.

---

## 1️⃣3️⃣ Purpose of:
### `%load_ext sql`
Loads SQL extension so Jupyter Notebook can run SQL commands.

### `%sql mysql+mysqlconnector://root:password@localhost/dbname`
This connects Notebook to your MySQL database.

---

## 1️⃣4️⃣ Types of CREATE TABLE
### 1. Simple table
```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50)
);
```

### 2. Table with constraints
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    salary INT
);
```

### 3. Table with foreign key
```sql
CREATE TABLE orders (
    id INT PRIMARY KEY,
    user_id INT,
    FOREIGN KEY(user_id) REFERENCES users(id)
);
```

---

## ✔ END OF DAY 01
Great work! Day 02 will continue with:
- SELECT
- WHERE
- ORDER BY
- LIMIT

