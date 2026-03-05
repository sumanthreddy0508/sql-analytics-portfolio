# Day 6 – SQL Basics

## Topics: `GROUP BY` and `HAVING`

These are used with aggregation functions like:

- `COUNT()`
- `SUM()`
- `AVG()`
- `MIN()`
- `MAX()`

---

## 1️⃣ `GROUP BY`

`GROUP BY` groups rows that have the same values in specified columns.

It is mostly used with aggregation functions.

### Example Table: `employees`

| id | name  | department | salary |
|---:|-------|------------|-------:|
| 1  | John  | IT         | 60000  |
| 2  | Sara  | HR         | 50000  |
| 3  | Mike  | IT         | 70000  |
| 4  | Anna  | Finance    | 55000  |
| 5  | David | IT         | 80000  |

### Example 1 – Count employees in each department

```sql
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department;
```

**Result**

| department | total_employees |
|------------|----------------:|
| IT         | 3               |
| HR         | 1               |
| Finance    | 1               |

### Example 2 – Average salary per department

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;
```

### Example 3 – Total salary per department

```sql
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department;
```

---

## 2️⃣ `HAVING`

`HAVING` is used to filter grouped results.

Think of it like:

- `WHERE` → filters rows
- `HAVING` → filters groups

### Example 4 – Departments with more than 1 employee

```sql
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department
HAVING COUNT(*) > 1;
```

**Result**

| department | total_employees |
|------------|----------------:|
| IT         | 3               |

### Example 5 – Departments with average salary above 60000

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;
```

---

## 🔹 `WHERE` vs `HAVING`

| Feature | `WHERE` | `HAVING` |
|--------|---------|----------|
| Used for | Filtering rows | Filtering groups |
| Used before | `GROUP BY` | After `GROUP BY` |
| Works with | Normal columns | Aggregate functions |

### Example

```sql
SELECT department, AVG(salary)
FROM employees
WHERE salary > 50000
GROUP BY department
HAVING AVG(salary) > 60000;
```
