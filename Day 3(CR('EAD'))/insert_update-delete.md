# Day 03 — DISTINCT, Removing Duplicates, INSERT, UPDATE, DELETE

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

---

# 3️⃣ INSERT — Add new data into table
INSERT is used to add rows.

### Syntax
```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

### Example
```sql
INSERT INTO students (id, name, age) VALUES (1, 'Naveen', 20);
```

Real-life (Amazon adding new product):
```sql
INSERT INTO products (name, price, stock) VALUES ('iPhone 16', 79999, 50);
```

---

# 4️⃣ UPDATE — Modify existing data
UPDATE is used to change already stored data.

### Syntax
```sql
UPDATE table_name SET column = value WHERE condition;
```

### Example
```sql
UPDATE students SET age = 21 WHERE id = 1;
```

Real-life (Changing your Swiggy address):
```sql
UPDATE users SET address = 'Trichy' WHERE id = 10;
```

⚠ WARNING: Always use WHERE!
If you forget:
```sql
UPDATE students SET age = 18;
```
All rows will be updated. (Very dangerous!)

---

# 5️⃣ DELETE — Remove data from table
DELETE removes records permanently.

### Syntax
```sql
DELETE FROM table_name WHERE condition;
```

### Example
```sql
DELETE FROM students WHERE id = 2;
```

Real-life (Deleting cart item in Soru Vandi backend):
```sql
DELETE FROM cart WHERE user_id = 5 AND item_id = 3;
```

⚠ WARNING: Never do this:
```sql
DELETE FROM students;
```
This will delete all rows.

---

# 6️⃣ Java Backend Real-Life Usage
### INSERT Example
When user signs up:
```sql
INSERT INTO users (name, email, password) VALUES (...);
```

### UPDATE Example
When user updates profile:
```sql
UPDATE users SET phone = '98765' WHERE id = 1;
```

### DELETE Example
When user removes cart item:
```sql
DELETE FROM cart WHERE cart_id = 12;
```

---

# 7️⃣ Interview Questions
1. What is DISTINCT and why is it used?
2. How do you remove duplicates from a table?
3. Difference between `DELETE` vs `TRUNCATE`?
4. What happens if you run UPDATE without WHERE?
5. Write a query to update salary of employee id=3.
6. Write a query to delete students age < 18.
7. Write an INSERT query with all columns.
8. Write an INSERT query with selected columns.
9. Can DELETE remove only specific rows? How?
10. What is the danger of DELETE without WHERE?

---

# 8️⃣ Homework
Create table:
```sql
CREATE TABLE employees (
  id INT,
  name VARCHAR(50),
  salary INT,
  age INT
);
```

Write:
1. INSERT 5 rows
2. UPDATE salary of id=1
3. DELETE employee age < 25
4. SELECT unique ages using DISTINCT
5. Remove duplicates using GROUP BY

---

# ✔ END OF DAY 03
Next topic (Day 4): **Joins (MOST IMPORTANT)**

