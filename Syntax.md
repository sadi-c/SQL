### Syntax

# SELECT: Used to query the database and retrieve data.

SELECT column1, column2 FROM table_name WHERE condition;

# The SELECT DISTINCT statement is used to return only distinct (different) values.

SELECT DISTINCT Country FROM Customers;

# The SELECT TOP clause is used to specify the number of records to return.

SELECT TOP 3 * FROM Customers;

# INSERT: Adds new data to a table.

INSERT INTO table_name (column1, column2) VALUES (value1, value2);

# UPDATE: Changes existing data in a table.

UPDATE table_name SET column1 = value1 WHERE condition;

# DELETE: Removes data from a table.

DELETE FROM table_name WHERE condition;


# GroupBy: groups rows that have the same values into summary rows
```

SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

# WHERE	Filters a result set to include only records that fulfill a specified condition

# IN Allows you to specify multiple values in a WHERE clause

```
SELECT * FROM Customers
WHERE Country IN ('Germany', 'France', 'US');
```

# VIEW	Creates, updates, or deletes a view

# UPDATE	Updates existing rows in a table

```
UPDATE Customers
SET ContactName='Juan';
```

# ORDER BY	Sorts the result set in ascending or descending order
``` 
SELECT * FROM Products
ORDER BY Price;
---
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;

```

# CREATE UNIQUE INDEX	Creates a unique index on a table (no duplicate values)
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);


# CASE	Creates different outputs based on conditions
```
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

# AND  Only includes rows where both conditions is true
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```


# AS  Renames a column or table with an alias 

# The PRIMARY KEY constraint uniquely identifies each record in a table. Primary keys must contain UNIQUE values, and cannot contain NULL values.

A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns (fields).

ALTER TABLE table_name
ADD COLUMN id INT AUTO_INCREMENT PRIMARY KEY;


The statement includes a column named "id" of type INT (integer) and sets it as the primary key, meaning it'll be utilized to identify each row within the table interestingly. The AUTO_INCREMENT keyword causes the column's value to increment automatically each time a new row is inserted into the table.

```
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    age INT
);

```
This statement creates a new " students " table with four columns: student_id, first_name, last_name, and age. The student_id column is set to be the PRIMARY KEY, meaning that it must contain a unique value for each row in the table.


# Side notes:

DDL (Data Definition Language): Defines database structures
Examples: 'CREATE TABLE', 'ALTER TABLE', 'DROP TABLE'

DML (Data Manipulation Language): Manipulates data within database structures
Examples: 'SELECT', 'INSERT', 'UPDATE', 'DELETE'

DCL (Data Control Language): Controls access to data
Examples: 'GRANT', 'REVOKE'

TCL (Transaction Control Language): Manages changes made by DML statements.
Examples: 'COMMIT', 'ROLLBACK'



