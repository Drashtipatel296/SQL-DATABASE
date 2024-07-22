# SQL-DATABASE

## Employee DBMS

## Setup
To set up the database, execute the following SQL script to create the employees table:

```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(300),
    role VARCHAR(250),
    salary INT
    age INT,
    address VARCHAR(300),
    phone VARCHAR(200)
);
```

## Add Multiple Employees with Selective Data

```sql
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Drashti Patel', 'CEO', 100000, 20, 'Surat', '9874563214');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Meshwa Patel', 'HR', 80000, 21, 'Surat', '8965231478');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Prapti Patel', 'Accountant', 60000, 25, 'Surat', '8523697412');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Sonal Patel', 'Manager', 95000, 22, 'Surat', '7896541236');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Dipali Gunjal', 'Manager', 60000, 19, 'Surat', '9517532864');
```

## Retrieve All Employee Information
```sql
SELECT * FROM employees;
```

## Find Employees with a Specific Role
```sql
SELECT * FROM employees WHERE role = 'Manager';
```

## Search for Employees with Names Containing "D"
```sql
SELECT * FROM employees WHERE LOWER(name) LIKE '%D%';
```

## Find Employees Older than 30 and Earning More than $70,000
```sql
SELECT * FROM employees WHERE age > 30 AND salary > 70000;
```

## Change the Salary of an Employee with ID 2
```sql
UPDATE employees SET salary = 90000 WHERE id = 2;
```

## Update the Address for Employees in the 'HR' Role
```sql
UPDATE employees SET address = 'New Address' WHERE role = 'HR';
```

## Remove an Employee with ID 4
```sql
DELETE FROM employees WHERE id = 4;
```

## Delete All Employees with Age Less than 20
```sql
DELETE FROM employees WHERE age < 20;
```
