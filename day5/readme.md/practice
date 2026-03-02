## 📊 Topic: COUNT, SUM, AVG, MIN, MAX (Aggregation Functions)

These are called **Aggregate Functions** because they return a **single value** from **multiple rows**.

---

### 1️⃣ `COUNT()` – Count Rows

**What it does:** Counts the number of rows.

**Syntax:**
```sql
SELECT COUNT(column_name)
FROM table_name;
```

**Examples:**

Count all employees:
```sql
SELECT COUNT(*)
FROM employees;
```

Count employees in IT department:
```sql
SELECT COUNT(*)
FROM employees
WHERE department = 'IT';
```

Count non-null salaries:
```sql
SELECT COUNT(salary)
FROM employees;
```

**Notes:**
- `COUNT(*)` counts **all rows**
- `COUNT(column)` ignores **NULL** values

---

### 2️⃣ `SUM()` – Total Value

**What it does:** Adds all values in a numeric column.

**Syntax:**
```sql
SELECT SUM(column_name)
FROM table_name;
```

**Examples:**

Total salary of all employees:
```sql
SELECT SUM(salary)
FROM employees;
```

Total IT department salary:
```sql
SELECT SUM(salary)
FROM employees
WHERE department = 'IT';
```

---

### 3️⃣ `AVG()` – Average Value

**What it does:** Returns the average of a numeric column.

**Examples:**

Average salary:
```sql
SELECT AVG(salary)
FROM employees;
```

Average salary in Toronto:
```sql
SELECT AVG(salary)
FROM employees
WHERE city = 'Toronto';
```

---

### 4️⃣ `MIN()` – Smallest Value

**What it does:** Returns the smallest value in a column.

**Example:**

Lowest salary:
```sql
SELECT MIN(salary)
FROM employees;
```

---

### 5️⃣ `MAX()` – Largest Value

**What it does:** Returns the largest value in a column.

**Example:**

Highest salary:
```sql
SELECT MAX(salary)
FROM employees;
```

---

## 🧠 Very Important: Using with `GROUP BY`

Aggregation becomes more powerful when combined with `GROUP BY`.

**Examples:**

Average salary per department:
```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```

Total salary per city:
```sql
SELECT city, SUM(salary)
FROM employees
GROUP BY city;
```
