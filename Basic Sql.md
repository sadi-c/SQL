### SQL Notes 

What is SQL?

SQL stands for Structured Query Language.
It is a standard programming language specifically designed for managing and manipulating relational databases.

###  Databases: 
- a database is a collection of data stored and structured in different database tables.

## Tables and columns:
- Each table has different columns which could contain different types of data.

For example, if you have a todo list reminder app, you would have a database, and in your database, you would have different tables storing different information like:

Users - In the users table, you would have some data for your users like: username, name, and active, for example.
Tasks - The tasks table would store all of the tasks that you are planning to do. The columns of the tasks table would be for example, task_name, status, due_date and priority.
The Users table will look like this:


```

+----+----------+---------------+--------+
| id | username | name          | active |
+----+----------+---------------+--------+
| 1  |    Smith | John Smith    |   true |
| 2  |  Venessa | Venessa Riite |   true |
| 3  |  devabdul| Dev Abdul    |  false |
+----+----------+---------------+--------+

```
Rundown of the table structure:

We have 4 columns: id, username, name and active.
We also have 3 entries/users.
The id column is a unique identifier of each user and is auto-incremented.

## Data Types:

CHAR: Fixed-length character string 
VARCHAR: Variable-length character string. Max size is specified in parenthesis.
TEXT: A string 
INTEGER or INT: a integer value 
BOOLEAN or BOOL: Holds a true or false value.
DATE: Holds a date
- DATE: Date (YYYY-MM-DD)
- TIME: Time (HH:MI)
- DATETIME: Date and time (YYYY-MM-DD HH:MI)
- TIMESTAMP: Date and time with timezone
- YEAR: Year

