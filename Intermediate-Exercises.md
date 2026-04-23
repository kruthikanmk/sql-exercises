# Intermediate Exercises
1.	Write a query to convert employee names to uppercase.

    `SELECT Upper(Emp_Name) 
    FROM Employee;`

2.	Write a query to find the length of each employee's name.

    `SELECT Emp_Name, LENGTH(Emp_Name) FROM Employee;`

3.	Write a query to extract the first three characters of each employee's name.

    `SELECT LEFT(Emp_Name, 3)
    FROM Employee;`

4.	Write a query to concatenate employee name and department with a hyphen.

    `SELECT CONCAT(Emp_Name,  '-', Department)
    FROM Employee;`

5.	Write a query to replace all occurrences of 'Manager' with 'Lead' in the role column.

    `SELECT REPLACE (Role, 'Manager', 'Lead')
    FROM Employee;`

6.	Write a query to trim leading and trailing spaces from project names.

    `SELECT TRIM(Project_Name)
    FROM Project;`

7.	Write a query to find employees whose names start with 'A'.

    ` SELECT * FROM Employee  
    WHERE Emp_Name LIKE 'A%';`

8.	Write a query to find employees whose names end with 'a'.

    `SELECT * FROM Employee  
    WHERE Emp_Name LIKE '%a';`

9.	Write a query to find employees whose names contain the letter 'e'.

    `SELECT * FROM Employee  
    WHERE Emp_Name LIKE '%e%';`

10.	Write a query to round the salary to the nearest thousand.

    `SELECT ROUND(Salary, 4)
    FROM Employee;`

11.	Write a query to find the absolute difference between two salaries.

    `SELECT * FROM Employee
    WHERE Abs ( Salary BETWEEN 50000 AND 70000);`

12.	Write a query to calculate the square root of the budget for each project.

    `SELECT SQRT(Budget)
    FROM Project;`

13.	Write a query to find the modulus of salary divided by 1000.

    `SELECT Salary % 1000 
    FROM Employee;`

14.	Write a query to convert the salary to a string format.

    `SELECT CAST(Salary AS CHAR) 
    FROM Employee;`

15.	Write a query to cast the budget column from integer to decimal.

    `SELECT CAST(Budget AS DECIMAL(10,2))
    FROM Project;`

16.	Write a query to extract the year from the hire_date.

    `SELECT EXTRACT(YEAR FROM Hire_Date)
    FROM Employee;`

17.	Write a query to extract the month from the hire_date.

    `SELECT EXTRACT(MONTH FROM Hire_Date)
    FROM Employee;`

18.	Write a query to extract the day from the hire_date.

    `SELECT EXTRACT(DAY FROM Hire_Date)
    FROM Employee;`

19.	Write a query to find the number of days between today and hire_date.

    `SELECT DATEDIFF(CURRENT_DATE, Hire_Date)
    FROM Employee;`

20.	Write a query to add 30 days to the hire_date.

    `SELECT DATE_ADD(Hire_Date, INTERVAL 30 DAY) 
    FROM Employee;`

21.	Write a query to subtract 1 year from the hire_date.
    `SELECT DATE_SUB(Hire_Date, INTERVAL 1 DAY)
    FROM Employee;`

22.	Write a query to format the hire_date as 'YYYY-MM-DD'.

    `SELECT DATE_FORMAT(Hire_Date, '%Y-%m-%d') 
    FROM Employee;`

23.	Write a query to find employees hired in the current year.

    `SELECT * FROM Employee
    WHERE YEAR(Hire_Date) = YEAR(CURRENT_DATE);`

24.	Write a query to find employees hired in the last 6 months.

    `SELECT * FROM Employee;
    WHERE Hire_Date >= DATE_SUB(CURRENT_DATE, INTERVAL 6 MONTH);`

25.	Write a query to convert a string '2023-01-01' to a date.

    `SELECT CAST('2023-01-01' AS DATE);`

26.	Write a query to convert a date to a string in 'MM/DD/YYYY' format.

    `SELECT DATE_FORMAT(Hire_Date, '%m/%d/%Y') 
    FROM Employee;`

27.	Write a query to find the ASCII value of the first character in employee names.

    `SELECT ASCII(Emp_Name) AS NumFirstChar
    FROM Employee;`

28.	Write a query to repeat the employee name 3 times.

    `SELECT REPEAT(Emp_Name, 3) 
    FROM Employee;`

29.	Write a query to pad employee names to 10 characters with trailing dots.

    `SELECT RPAD(Emp_Name, 10, '.') 
    FROM Employee;`

30.	Write a query to find the position of 'a' in employee names.

    `SELECT POSITION('a' IN Emp_Name) 
    FROM Employee;`
