# Day 02 — SQL SELECT (Basics to Strong Foundation)
---

# 1️⃣ What is SELECT?
`SELECT` is the MOST IMPORTANT command in SQL.
It is used to **get data** from a table.

Think of SELECT like:
- Searching a product in Amazon
- Searching restaurant in Swiggy
- Checking your chats in WhatsApp

All these apps internally run a SELECT query.

---

# 2️⃣ Basic SELECT Syntax
```sql
SELECT column1, column2 FROM table_name;
```

Get all columns:
```sql
SELECT * FROM table_name;
```

---

# 3️⃣ Real-Life Example
When you open Swiggy and see all restaurants:
```sql
SELECT * FROM restaurants;
```

When you search "Biryani":
```sql
SELECT * FROM menu_items WHERE name = 'Biryani';
```

---

# 4️⃣ SELECT with Specific Columns
```sql
SELECT name, age FROM students;
```
This shows only 2 columns.

---

# 5️⃣ SELECT with WHERE (Filtering)
Used to get only matching data.

Example:
```sql
SELECT * FROM students WHERE age = 20;
```

Another:
```sql
SELECT * FROM employees WHERE salary > 30000;
```

---

# 6️⃣ SELECT with ORDER BY (Sorting)
```sql
SELECT * FROM employees ORDER BY salary DESC;
```
- ASC → small to big
- DESC → big to small

Real-life:
Sorting restaurants by rating:
```sql
SELECT * FROM restaurants ORDER BY rating DESC;
```

---

# 7️⃣ SELECT with LIMIT
Used to control number of rows.

```sql
SELECT * FROM students LIMIT 3;
```

Real-life:
When Amazon shows "Top 5 deals":
```sql
SELECT * FROM products ORDER BY discount DESC LIMIT 5;
```

---

# 8️⃣ SELECT with Conditions
### Equals
```sql
WHERE age = 20
```

### Greater than
```sql
WHERE salary > 50000
```

### Not equal
```sql
WHERE age <> 18
```

### AND
```sql
SELECT * FROM employees WHERE age > 25 AND salary > 30000;
```

### OR
```sql
SELECT * FROM employees WHERE age = 20 OR age = 22;
```

### BETWEEN
```sql
SELECT * FROM products WHERE price BETWEEN 100 AND 500;
```

### LIKE (Search)
```sql
SELECT * FROM users WHERE name LIKE 'A%';
```
Finds names starting with A.

Real-life:
When you type "Na" and it shows "Naveen":
```sql
SELECT * FROM users WHERE name LIKE 'Na%';
```

---

# 9️⃣ SELECT + Real Backend Use (Java + API)
When React sends a request:
GET: `/restaurants`

Java runs:
```sql
SELECT * FROM restaurants;
```

When React filters by rating:
```sql
SELECT * FROM restaurants WHERE rating > 4;
```

---

# 🔟 Interview Questions for SELECT
1. What is SELECT?
2. Difference between `SELECT *` and selecting specific columns.
3. What is WHERE clause?
4. What is ORDER BY? ASC vs DESC?
5. What is LIMIT used for?
6. How does LIKE work?
7. What is the difference between AND vs OR?
8. What is the use of DISTINCT?
9. How to remove duplicates with SELECT?
10. What is the difference between filtering and sorting?

---
# 1️⃣ What is the use of DISTINCT?
`DISTINCT` is used to remove duplicate values from the output.

It shows only **unique** values.

### Example Table: students
| name  | age |
|-------|-----|
| Naveen | 20 |
| Arjun  | 20 |
| Naveen | 21 |

### Query without DISTINCT:
```sql
SELECT name FROM students;
```
Output:
```
Naveen
Arjun
Naveen
```

### Query with DISTINCT:
```sql
SELECT DISTINCT name FROM students;
```
Output:
```
Naveen
Arjun
```

Real-life example:
When Swiggy shows all **unique cuisines**:
```sql
SELECT DISTINCT cuisine FROM restaurants;
```

---

# 2️⃣ How to remove duplicates with SELECT?
The simplest way:
```sql
SELECT DISTINCT column_name FROM table_name;
```

Example:
```sql
SELECT DISTINCT age FROM students;
```
Shows all unique ages.

### Remove duplicates using GROUP BY
```sql
SELECT name FROM students GROUP BY name;
```

### Remove duplicates based on multiple columns
```sql
SELECT DISTINCT name, age FROM students;
```

# 1️⃣1️⃣ Homework (Simple Practice)
Create table:
```sql
CREATE TABLE students (
  id INT,
  name VARCHAR(50),
  age INT,
  marks INT
);
```

---

Insert some sample data.

Write queries:
1. Find students age above 20
2. Find students marks below 50
3. Find all students sorted by marks descending
4. Show only first 2 students
5. Show students whose name starts with 'N'

---

# ✔ END OF DAY 02
Next Topic (Day 3): **INSERT, UPDATE, DELETE**

