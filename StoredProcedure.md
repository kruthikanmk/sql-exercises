# Stored Procedure 
A stored procedure is a precompiled SQL code that can be saved and reused.

A stored procedure is also have parameters, it can act based on the parameters values that is passed.

## Benefits of Stored Procedure
1. Code Reuseability :- The same procedure can be called from various applications.

2. Improved performance :- Stored procedure are precompiled and run faster.

3. Database Sercuity :- To set user permission to run a specific procedure.

4. Easy Maintenance :- When update a procedure, it automatically update.

## Syntax for Stored Procedure 

create procedure procedure_name

@param1 datatype,@param2 datatype

AS 

Begin

Select column1,column2
from table_name
where columnN=@paramN;

End;

### Example 
create procedure GetCustomerByCity

@city nvarchar(50)

AS

Begin 

Select * from 

Customers 

where City=@City;

End;

"Customers" table


## Execute a Stored Procedure

To run a stored procedure, use the EXEC statement

EXEC procedure_name @param1='value1', @param2='value2';

## Drop a Stored Procedure

To delete a stored procedure, use the DROP PROCEDURE statement

DROP PROCEDURE procedure_name;

To ensure that DROP PROCEDURE does not return an error, if the procedure is missing, add the IF EXISTS clause

DROP PROCEDURE IF EXISTS procedure_name;

## Exercises
1. What is the primary purpose of a stored procedure in SQL?

    To save reusable SQL code for repeated use

2. Which of the following is the correct syntax to create a stored procedure?

    CREATE PROCEDURE procedure_name AS BEGIN sql_statement END;

3. How do you execute a stored procedure named GetCustomers?

    EXEC GetCustomers;

4. What is the purpose of the @City parameter in the following stored procedure?

   CREATE PROCEDURE SelectCustomers @City nvarchar(50)
   AS
   BEGIN
   SELECT * FROM Customers WHERE City = @City
   END;

   To specify a variable for the City filter in the query


5. Drag and drop the correct syntax to create a stored procedure with multiple parameters.
  
    CREATE PROCEDURE SelectAllCustomers @City nvarchar(30), @PostalCode nvarchar(10)
    AS BEGIN 
    SELECT * FROM Customers WHERE City = @City AND PostalCode = @PostalCode
    ;
    END;

6. Which of the following is a valid way to execute a stored procedure with two parameters?

   EXEC GetCustomerDetails @City = 'London', @PostalCode = 'WA1 1DP';

## SQL Server Agent

SQL Server is a popular Relational Database Management System (RDBMS).It uses Structured Query Language (SQL), making storing, retrieving, manipulating, and analyzing data much easier.

