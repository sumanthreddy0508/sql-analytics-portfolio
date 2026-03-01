# Day 4 – SQL Basics  
**Topics:** `ORDER BY`, `DISTINCT`, `LIMIT / TOP`  
**Date:** 2026-03-01  

---

## 1) ORDER BY (Sorting Data)

### What it does
`ORDER BY` is used to sort your result in **ascending** or **descending** order.

### Syntax
```sql
SELECT column_name
FROM table_name
ORDER BY column_name ASC|DESC;
```

- `ASC` → Ascending (**default**)
- `DESC` → Descending

### Example 1: Sort by salary (low → high)
```sql
SELECT name, salary
FROM Employees
ORDER BY salary ASC;
```

**What happens?**
- SQL selects `name` and `salary`
- Then sorts the result
- Lowest salary comes first

### Example 2: Sort by salary (high → low)
```sql
SELECT name, salary
FROM Employees
ORDER BY salary DESC;
```

Now the highest salary appears at the top.

### Example 3: Sort by multiple columns
```sql
SELECT name, department, salary
FROM Employees
ORDER BY department ASC, salary DESC;
```

**How it works**
- First sorts by `department` (A–Z)
- Inside each department → sorts `salary` high to low  
- Sorting happens **left to right**

---

## 2) DISTINCT (Remove Duplicates)

### What it does
`DISTINCT` removes duplicate values.

### Example 1: Unique departments
```sql
SELECT DISTINCT department
FROM Employees;
```

If `IT` appears 10 times → it shows only once.

### Example 2: Unique city + department combination
```sql
SELECT DISTINCT city, department
FROM Employees;
```

SQL checks duplicates based on **both columns together**.

### Important
- `DISTINCT` applies to the **entire row combination**
- Not just one column when multiple columns are selected

---

## 3) LIMIT / TOP (Restrict Rows)

Sometimes we don’t want all rows — only the top few.

### MySQL / PostgreSQL → LIMIT
```sql
SELECT *
FROM Employees
ORDER BY salary DESC
LIMIT 5;
```

**What happens?**
- Sort salary high → low
- Take only the first 5 rows

### SQL Server → TOP
```sql
SELECT TOP 5 *
FROM Employees
ORDER BY salary DESC;
```

Same logic, different keyword.

### Important concept
If you use `LIMIT` or `TOP` **without** `ORDER BY`:

```sql
SELECT TOP 5 * FROM Employees;
```

You get a **random** 5 rows.

✅ Always combine:

- `ORDER BY + LIMIT/TOP`

for meaningful results.

---

## 4) Combining Everything

### Example: Top 3 highest paid IT employees
```sql
SELECT *
FROM Employees
WHERE department = 'IT'
ORDER BY salary DESC
LIMIT 3;   -- Use TOP 3 for SQL Server
```

### Execution order
1. `FROM` → Employees  
2. `WHERE` → Only IT employees  
3. `ORDER BY` → Salary high to low  
4. `LIMIT` → First 3 rows  
