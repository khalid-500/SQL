# SQL

# Create Table 
```javascript
CREATE TABLE table_name (
    column1 datatype Property,
    column2 datatype  Property,
    column3 datatype,
);
```
# Datatype 
|        String       |       Integer      |    Fixed Value    |   BOOLEAN    |             TIMESTAMPTZ              |     Text      |    Priimery Key   |
| ------------------- | ------------------ | ------------------| -------------| -------------------------------------|-------------- |-----------------  |
|     varchar(255)    |        int         |  ENUM(val1, val2) |   BOOLEAN    |       NOT NULL DEFAULT NOW()         |     text      |      UUID         |

# PROPERTY 

|      NOT NULL           |       AUTO_INCREMENT      |          UNIQUE     |                CHECK (Age>=18)                    |
| ----------------------  | ------------------------- | --------------------| --------------------------------------------------|

|    DEFAULT 'Sandnes'    |        PRIMARY KEY        |  FOREIGN KEY (Primery Key Column) REFERENCES Persons(Frogen Key Column) |   
|-------------------------|---------------------------|-------------------------------------------------------------------------|




# SELECT
```javascript
$$ Use To Get All Object In The Table 

//Select All Column 
SELECT * FROM users;

//Select Specific Column like Attribute In Sequlize
SELECT first_name, last_name FROM users;

//Create new Outpot For The Column
SELECT CONCAT(first_name, ' ', last_name) AS 'Name', dept FROM users;

$$ The SQL SELECT DISTINCT Statement
//Get Just The Uniqe Value
SELECT DISTINCT column1, column2, ...
FROM table_name;


```

# WHERE
```javascript
$$ Use To Get Specific Object In Table Where The property Match 

//Get The Data Where Have Specific Property
SELECT * FROM users WHERE location='Massachusetts';

//Get The Data Where Have Multibule Proberty
SELECT * FROM users WHERE location='Massachusetts' AND dept='sales' AND dept='sales' AND dept='sales';

//select the element where not equal attribute
SELECT * FROM users WHERE NOT condition;

```

# DELETE

```javascript
// DELETE Statement Delete Object From Table
DELETE FROM table_name WHERE condition;

// DROP TABLE Statement
DROP TABLE table_name;

// DROP DATABASE Statement
DROP DATABASE databasename;

```
# Update Row
```javascript
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;
```

# Order By (Sort)
```javascript
SELECT * FROM users ORDER BY last_name ASC;
SELECT * FROM users ORDER BY last_name DESC;

```

# Join SQL

## Inner Join 
![](https://mulham.github.io/assets/sql_inner-join.gif)

##### The INNER JOIN keyword selects records that have matching values in both tables. 
```javascript
SELECT *
FROM Orders
INNER JOIN NameTable ON TableName.PrimeryKey = OtherTable.ForginKey
INNER JOIN Shippers ON TableName.PrimeryKey = OtherTable.ForginKey;
```

## SQL LEFT JOIN Keyword
![](https://mulham.github.io/assets/sql_left-join.gif)
##### The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.


```javascript
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;

```

## SQL RIGHT JOIN Keyword
![](https://mulham.github.io/assets/sql_rightjoin.gif)
##### The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.

```javascript
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;

```

## SQL FULL OUTER JOIN Keyword
![](https://mulham.github.io/assets/sql_full-join.gif)
##### The FULL OUTER JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.

```jaavsript
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;

```


## JSON Array from SQL
```javascript 

    //Select All Property From Main Table 
    select fullname,
    
    //Select The Other Table AS array inside the object  
    (select array_to_json(array_agg(row_to_json(postes_alias)))
    from (select * from postes where persondopostid = regusterid)postes_alias) as postess
    
    //All Data Will Git From The Main 
    from regusters;


```
