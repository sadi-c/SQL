#### The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country"

The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns
```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
``` 

Output:

```
Number of Records: 9
Expr1000	Country
13 	        USA 
11 	        France 
11 	        Germany 
9 	        Brazil 
7 	        UK 
5 	        Mexico 
5 	        Spain 
4 	        Venezuela 
3 	         Canada 

```

#### A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;


 - Different Types of SQL JOINs
Here are the different types of the JOINs in SQL:

 - (INNER) JOIN: Returns records that have matching values in both tables
 - LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
 - RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
- FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table



#### The cast function converts a data type into another data type.

Cast Function Example:
SELECT Cast(10 AS VARCHAR); 

Output:

'10'

#### The coalesce function returns the first non-null value from a list of expressions.

Coalesce Function Example:
SELECT COALESCE(NULL, 'value2', 'value3'); 

Output:

'value2'

#### The is null function checks if an expression is null; if it is, it returns a replacement value.

Is Null Function Example:
SELECT Isnull('value', 'null'); 

Output:

'value'

#### The if null function is similar to the is null function, but the arguments are reversed.

If Null Function Example:
SELECT Ifnull('value', 'null'); 

Output:

'value'


#### The case expression performs conditional operations based on a specified expression.

Case Expression Example:
SELECT CASE
         WHEN 1 = 1 THEN 'true'
         ELSE 'false'
       END; 

Output:

'true'



#### The convert function converts a value into a specified data type.

Convert Function Example:
SELECT CONVERT(VARCHAR, 10); 

Output:

'10'


#### The split function splits a string into a table of substrings.

Split Function Example:
SELECT *
FROM   String_split('apple,banana,cherry', ','); 

Output:

apple banana cherry


#### The random function generates a random number between 0 and 1.

Random Function Example:
SELECT Rand(); 

Output:

0.230985738392902

#### The if function performs a conditional operation based on a specified expression.

If Function Example:
SELECT IF(1 = 1, 'true', 'false'); 

Output:

'True'


#### SELECT Dateadd(day, 7, '2023-05-05'); 

Output:

'2023-05-12'


#### The date format function reformats a date value into a string with a specified format.

Date Format Example:
SELECT Date_format('2024-03-03', '%m/%d/%Y'); 

Output:

'03/03/2024'


#### The date part function extracts a specified part of a date, such as year, month, or day.

Date Part Example:
SELECT Datepart(year, '2024-05-29'); 

Output:

2024


#### The length function is used to return the length of a string.

Length Function Example:
SELECT Len('mango'); 

Output:

5


#### SELECT LEFT('banana', 3); 

Output:

'ban'


#### The trim function removes leading and trailing spaces from a string.

Trim Function Example:
SELECT Trim(' banana ');

Output:

'banana'

##### The concatenate function links two or more strings together.

Concat Function Example:
SELECT Concat('mango', 'banana', 'cherry'); 

Output: 

'mangobananacherry'

#### The format function reformats a value into a specified string format.

Format Function Example:
SELECT Format(12345.6789, '#,##0.00'); 

Output:

12,345.68


#### SELECT Replace('banana', 'a', 'e'); 

Output:

Benene


#### Creates a unique index on a table. Duplicate values are not allowed:
Below creates an index named "idx_lastname" on the "LastName" column in the "Persons" table:

CREATE INDEX idx_lastname
ON Persons (LastName);




