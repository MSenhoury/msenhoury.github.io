---
title: "Learn SQL for Data Science"
date: 2025-03-02
type: "docs"
math: true
tags:
  - SQL
  - Database
  - Data Science
  - Python
image:
  caption: "Master SQL step by step with easy examples."
bio: "Learn SQL for data manipulation and analysis!"
---

# **Learn SQL for Data Science** 🚀  
A beginner-friendly introduction to **SQL (Structured Query Language)**. Master **database queries, data manipulation, and advanced operations** step by step!

---

## 🟢 **Lesson 1: Introduction to SQL**
SQL (Structured Query Language) is a language designed for **managing and querying data in relational databases**.

### **Why Learn SQL?**  
✅ SQL is used in **Data Science & Analytics**  
✅ Helps in **storing and retrieving large datasets**  
✅ **Most companies use SQL** for managing business data  

📝 **Mathematical Structure of a Table:**  
A **table** in SQL can be represented as a **matrix**:

\[
T = \begin{bmatrix} 
\text{ID} & \text{Name} & \text{Age} \\ 
1 & \text{Alice} & 25 \\ 
2 & \text{Bob} & 30 \\ 
3 & \text{Charlie} & 35 
\end{bmatrix}
\]

Each **row** is a **record**, and each **column** is a **field**.

---

## 🟢 **Lesson 2: Creating a Database and a Table**
To start using SQL, you need a **database**.

📌 **Create a Database:**
```sql
CREATE DATABASE my_database;
```

📌 **Create a Table:**
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    department VARCHAR(50)
);
```
📝 **Mathematical Representation:**
\[
\text{employees}(id, name, age, department)
\]
where **\( id \)** is the **Primary Key (PK)**, ensuring uniqueness.

---

## 🟢 **Lesson 3: Inserting and Retrieving Data**
📌 **Insert Data into Table:**
```sql
INSERT INTO employees (id, name, age, department) VALUES
(1, 'Alice', 25, 'HR'),
(2, 'Bob', 30, 'IT'),
(3, 'Charlie', 35, 'Finance');
```

📌 **Retrieve All Data:**
```sql
SELECT * FROM employees;
```

📌 **Retrieve Specific Columns:**
```sql
SELECT name, age FROM employees;
```

📝 **Mathematical Interpretation:**  
SQL **queries** act as **functions** on a dataset:

\[
\text{SELECT } f_1, f_2, ... f_n \text{ FROM } T
\]

where \( f_1, f_2, ... f_n \) are column names and \( T \) is the table.

---

## 🟢 **Lesson 4: Filtering Data with WHERE Clause**
📌 **Find employees older than 30:**
```sql
SELECT * FROM employees WHERE age > 30;
```

📌 **Find employees in the IT department:**
```sql
SELECT * FROM employees WHERE department = 'IT';
```

📌 **Find employees whose name starts with 'A':**
```sql
SELECT * FROM employees WHERE name LIKE 'A%';
```

📝 **Mathematical Condition:**
\[
\text{SELECT * FROM employees WHERE } \text{age} > 30
\]

SQL processes conditions like mathematical inequalities.

---

## 🟢 **Lesson 5: Aggregation (SUM, AVG, COUNT)**
📌 **Find the average age of employees:**
```sql
SELECT AVG(age) FROM employees;
```

📌 **Count total employees:**
```sql
SELECT COUNT(*) FROM employees;
```

📌 **Find the sum of all ages:**
```sql
SELECT SUM(age) FROM employees;
```

📝 **Mathematical Formulas:**
- **Average Age:**
\[
\text{AVG(age)} = \frac{\sum_{i=1}^{n} \text{age}_i}{n}
\]
- **Total Employees:**
\[
\text{COUNT(*)} = n
\]

---

## 🟢 **Lesson 6: Grouping and Sorting Data**
📌 **Group employees by department and count them:**
```sql
SELECT department, COUNT(*) FROM employees GROUP BY department;
```

📌 **Sort employees by age (ascending):**
```sql
SELECT * FROM employees ORDER BY age ASC;
```

📌 **Sort employees by name (descending):**
```sql
SELECT * FROM employees ORDER BY name DESC;
```

📝 **Mathematical Representation of Grouping:**
\[
\text{GROUP BY } X \Rightarrow f: X \to \sum(Y)
\]

Grouping maps **unique values in column \( X \)** to the **sum/count of values in column \( Y \)**.

---

## 🟢 **Lesson 7: SQL Joins – Combining Tables**
In relational databases, **JOINs** help merge tables.

📌 **Example: Employee & Salary Tables**
```sql
CREATE TABLE salaries (
    id INT,
    salary INT,
    FOREIGN KEY (id) REFERENCES employees(id)
);
```

📌 **Inner Join: Match employees with their salaries**
```sql
SELECT employees.name, employees.department, salaries.salary
FROM employees
INNER JOIN salaries ON employees.id = salaries.id;
```

📌 **Left Join: Keep all employees, even if they have no salary**
```sql
SELECT employees.name, salaries.salary
FROM employees
LEFT JOIN salaries ON employees.id = salaries.id;
```

📝 **Mathematical Interpretation:**
\[
T_{\text{employees}} \bowtie T_{\text{salaries}}
\]

A **JOIN** is a **Cartesian product** followed by a **filtering condition**.

---

## 🟢 **Lesson 8: Subqueries – Queries Inside Queries**
📌 **Find employees earning more than the average salary:**
```sql
SELECT name, salary FROM salaries
WHERE salary > (SELECT AVG(salary) FROM salaries);
```

📌 **Find the youngest employee:**
```sql
SELECT * FROM employees
WHERE age = (SELECT MIN(age) FROM employees);
```

📝 **Mathematical Interpretation:**
\[
\text{SELECT * FROM } T \text{ WHERE } x = \min(x)
\]

---

## 🎯 **Final Challenge: Build a Mini HR Database**
Now, **try to create your own database** and **write queries** for it!

📌 **Tasks:**
1. Create an `employees` table with name, age, and department.
2. Create a `salaries` table with employee ID and salary.
3. Write queries to:
   - Find the **highest-paid employee**.
   - Get the **average salary by department**.
   - List **employees older than 30, ordered by salary**.

---

## 🎉 **Congratulations! You Learned SQL!**
✅ You learned **basic SQL queries**  
✅ You mastered **filtering, sorting, and aggregating data**  
✅ You understood **Joins and Subqueries**  

🚀 **Next Steps:**
🔹 Learn **Advanced SQL (Window Functions, Indexing, Optimization)**  
🔹 Use **SQL in Data Science with Pandas & Python**  
🔹 Practice on **[LeetCode SQL Problems](https://leetcode.com/problemset/database/)**  

---

📩 **Need help? Contact me at** [m.asenhoury@hotmail.com](mailto:m.asenhoury@hotmail.com)  
💡 **Follow my work on GitHub:** [github.com/mohamed-senhoury](https://github.com/mohamed-senhoury)
```

---

### ✅ **Why This Lesson?**
✔ **Follows the same structure as your Python/NLP lessons**  
✔ **Covers SQL from basics to advanced queries**  
✔ **Includes real-world data science applications**  
✔ **Uses math formulas to explain SQL logic**  