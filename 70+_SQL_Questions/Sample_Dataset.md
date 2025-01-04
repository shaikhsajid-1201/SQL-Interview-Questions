## Schema 
```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    name VARCHAR(100),
    first_name VARCHAR(50),
    email VARCHAR(100),
    department_id INT,
    job_title VARCHAR(100),
    job_role VARCHAR(100),
    manager_id INT,
    salary DECIMAL(10,2),
    join_date DATE,
    birth_date DATE,
    bonus DECIMAL(10,2)
);

CREATE TABLE departments (
    department_id INT PRIMARY KEY,
    department_name VARCHAR(100)
);

CREATE TABLE sales (
    sale_id INT PRIMARY KEY,
    customer_id INT,
    sales_amount DECIMAL(10,2),
    sale_date DATE
);
```

## Dataset
```sql
-- Inserting sample departments
INSERT INTO departments (department_id, department_name) VALUES 
(101, 'Sales'),
(102, 'Marketing'),
(103, 'Engineering');

-- Inserting sample employees
INSERT INTO employees (
    employee_id, name, first_name, email, department_id, 
    job_title, job_role, manager_id, salary, join_date, birth_date, bonus
) VALUES 
(1, 'John Anderson', 'John', 'john@example.com', 101, 'Sales Manager', 'Manager', NULL, 100000, '2015-03-15', '1985-06-20', 15000),
(2, 'Sarah Smith', 'Sarah', 'sarah@example.com', 101, 'Sales Representative', 'Sales', 1, 65000, '2018-07-01', '1990-11-10', 8000),
(3, 'Michael Brown', 'Michael', 'michael@example.com', 102, 'Marketing Director', 'Manager', NULL, 95000, '2016-02-10', '1988-04-05', 12000),
(4, 'Emily Davis', 'Emily', 'emily@example.com', 102, 'Marketing Specialist', 'Marketing', 3, 60000, '2019-05-20', '1992-09-15', 7500),
(5, 'David Wilson', 'David', 'david@example.com', 103, 'Senior Engineer', 'Engineering', NULL, 110000, '2014-11-05', '1983-12-30', 18000),
(6, 'Jennifer Lee', 'Jennifer', 'jennifer@example.com', 103, 'Software Engineer', 'Engineering', 5, 75000, '2017-08-15', '1991-07-25', 10000),
(7, 'Robert Taylor', 'Robert', 'robert@example.com', 101, 'Sales Executive', 'Sales', 1, 80000, '2016-09-01', '1987-03-12', 11000);

-- Inserting sample sales data
INSERT INTO sales (sale_id, customer_id, sales_amount, sale_date) VALUES 
(1, 101, 5000.00, '2024-01-15'),
(2, 102, 7500.00, '2024-02-20'),
(3, 101, 6200.00, '2024-03-10'),
(4, 103, 9000.00, '2024-04-05'),
(5, 102, 4800.00, '2024-05-18');
```
