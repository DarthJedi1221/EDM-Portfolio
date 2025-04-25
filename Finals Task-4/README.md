# Finals Task 4 - Employee Databases
## Task 1 - Query Statements
SELECT * FROM EmployeeSalaries;

SELECT * FROM EmployeeData;
## Task 2 - Table Structure
CREATE DATABASE payroll; USE payroll;

CREATE TABLE EmployeeSalaries ( employee_id INT AUTO_INCREMENT PRIMARY KEY, employee_name VARCHAR(100), department VARCHAR(50), salary DECIMAL(10,2), hire_date DATE );

INSERT INTO EmployeeSalaries (employee_name, department, salary, hire_date) VALUES ('John Smith', 'Sales', 75000.00, '2017-05-15'), ('Jane Doe', 'Marketing', 85000.00, '2018-03-20'), ('Michael Johnson', 'Sales', 90000.00, '2016-08-10'), ('Emily Brown', 'HR', 65000.00, '2019-01-05'), ('David Wilson', 'Marketing', 80000.00, '2017-10-25'), ('Jennifer Lee', 'IT', 95000.00, '2015-06-30'), ('Christopher Davis', 'Sales', 70000.00, '2020-02-12'), ('Jessica Martinez', 'IT', 105000.00, '2014-09-18'), ('Andrew Taylor', 'Marketing', 75000.00, '2018-07-15'), ('Elizabeth Anderson', 'HR', 60000.00, '2020-04-01'), ('Daniel Thomas', 'IT', 98000.00, '2017-12-10'), ('Sarah White', 'Sales', 82000.00, '2019-08-05'), ('Kevin Garcia', 'HR', 70000.00, '2016-03-08'), ('Laura Martinez', 'Marketing', 88000.00, '2017-04-22'), ('Robert Lopez', 'IT', 93000.00, '2018-11-15'), ('Amanda Harris', 'Sales', 78000.00, '2018-09-30');

CREATE DATABASE employeeDB; USE employeeDB;

CREATE TABLE EmployeeData ( employee_id INT AUTO_INCREMENT PRIMARY KEY, full_name VARCHAR(100), department VARCHAR(50), salary DECIMAL(10,2), hire_date DATE, manager_id INT );

INSERT INTO EmployeeData (full_name, department, salary, hire_date, manager_id) VALUES ('John Smith', 'Sales', 75000.00, '2017-05-15', NULL), ('Jane Doe', 'Marketing', 85000.00, '2018-03-20', NULL), ('Michael Johnson', 'Sales', 90000.00, '2016-08-10', 1), ('Emily Brown', 'HR', 65000.00, '2019-01-05', NULL), ('David Wilson', 'Marketing', 80000.00, '2017-10-25', 2), ('Jennifer Lee', 'IT', 95000.00, '2015-06-30', NULL), ('Christopher Davis', 'Sales', 70000.00, '2020-02-12', 3), ('Jessica Martinez', 'IT', 105000.00, '2014-09-18', 6), ('Andrew Taylor', 'Marketing', 75000.00, '2018-07-15', 2), ('Elizabeth Anderson', 'HR', 60000.00, '2020-04-01', 4), ('Daniel Thomas', 'IT', 98000.00, '2017-12-10', 6), ('Sarah White', 'Sales', 82000.00, '2019-08-05', 1), ('Kevin Garcia', 'HR', 70000.00, '2016-03-08', 5), ('Laura Martinez', 'Marketing', 188000.00, '2017-04-22', 4), ('Robert Lopez', 'IT', 193000.00, '2018-11-15', 9), ('Amanda Harris', 'Sales', 128000.00, '2018-09-30', 1);

## Task 3 - Relational Schema for Products Table
<img width="434" alt="Task3Po" src="https://github.com/user-attachments/assets/940deeea-16d5-4423-80dd-beb016ffea0e" />


## Task 4 - SQL Copy of the Database and Table Structures
<img width="347" alt="Task4" src="https://github.com/user-attachments/assets/dcf8fc19-b418-4c11-857e-9ece33cca37f" />
