The whole purpose of JOIN statements is to allow us to pull data from more than one table at a time.

JOINs are useful for allowing us to pull data from multiple tables. This is both simple and powerful all at the same time.

With the addition of the JOIN statement to our toolkit, we will also be adding the ON statement.

We use ON clause to specify a JOIN condition which is a logical statement to combine the table in FROM and JOIN statements.

Ex 1. Try pulling all the data from the accounts table, and all the data from the orders table.

```
SELECT orders.*, accounts.*
FROM accounts
JOIN orders
ON accounts.id = orders.account_id;

```

Ex 2. Try pulling standard_qty, gloss_qty, and poster_qty from the orders table, and the website and the primary_poc from the accounts table.

```
SELECT orders.standard_qty, orders.gloss_qty, 
          orders.poster_qty,  accounts.website, 
          accounts.primary_poc
FROM orders
JOIN accounts
ON orders.account_id = accounts.id
```

INNER JOINS
An inner join between two tables will return only records where a joining field, such as a key, finds a match in both tables.

INNER JOIN join ON one field

```
SELECT *
FROM ARTIST AS ART
INNER JOIN ALBUM AS ALB
ON ART.ARTIST_ID = ALB.ARTIST_ID;
```

INNER JOIN with USING

```
SELECT *
FROM ARTIST AS ART
INNER JOIN ALBUM AS ALB
USING (ARTIST_ID);

```

LEFT JOIN
A left join keeps all of the original records in the left table and returns missing values for any columns from the right table where the joining field did not find a match.

LEFT JOIN on one field

```
SELECT *
FROM ARTIST AS ART
LEFT JOIN ALBUM AS ALB
ON ART.ARTIST_ID = ALB.ARTIST_ID;
```

RIGHT JOIN
A right join keeps all of the original records in the right table and returns missing values for any columns from the left table where the joining field did not find a match. Right joins are far less common than left joins, because right joins can always be re-written as left joins.


RIGHT JOIN on one field
```
SELECT *
FROM ARTIST AS ART
RIGHT JOIN ALBUM AS ALB
ON ART.ARTIST_ID = ALB.ARTIST_ID;
```