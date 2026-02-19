===Day 2	SQL Basics	SELECT, WHERE, Comparison Operators	Upload filtering practice file	====

Select : used to retrieve the data from the table
ex:
select column1 from tablename;

if we need all the columns from the table
then select * from table name;

where: used for filtering records or rows based on the conditions

| Operator | Meaning               |
| -------- | --------------------- |
| =        | Equal                 |
| != or <> | Not equal             |
| >        | Greater than          |
| <        | Less than             |
| >=       | Greater than or equal |
| <=       | Less than or equal    |


=====practice i did:============

create database companydb;
use companydb;
CREATE TABLE employees (
    emp_id INT,
    name VARCHAR(50),
    department VARCHAR(50),
    salary INT,
    city VARCHAR(50)
);

INSERT INTO employees VALUES
(1, 'Rahul', 'IT', 60000, 'Toronto'),
(2, 'Anita', 'HR', 45000, 'Vancouver'),
(3, 'John', 'IT', 75000, 'Toronto'),
(4, 'Meera', 'Finance', 50000, 'Calgary'),
(5, 'David', 'HR', 40000, 'Vancouver');


-- Show all employees from IT department 
Select name from employees
where department='it';

-- Show employees with salary greater than 50000.
Select * from employees
where salary>50000;

-- Show employees from Vancouver.
Select * from employees
where city='vancouver';

-- Show employees with salary less than or equal to 50000.
Select * from employees
where salary<=50000;
-- Show employees from HR department.
Select name from employees
where department='hr';
-- Show employees from Toronto with salary > 60000.
Select * from employees
where city='toronto'
and salary>60000;






