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
|        String       |       Integer      |    Fixed Value    |   BOOLEAN    |             TIMESTAMPTZ              |
| ------------------- | ------------------ | ------------------| -------------| -------------------------------------|
|     varchar(255)    |        int         |  ENUM(val1, val2) |   BOOLEAN    |       NOT NULL DEFAULT NOW()         |

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


# Join Sql 
![](https://mulham.github.io/assets/sql_inner-join.gif)
![](data:image/png;base64,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)

## Inner Join 
##### The INNER JOIN keyword selects records that have matching values in both tables. 
```javascript
SELECT *
FROM Orders
INNER JOIN NameTable ON TableName.PrimeryKey = OtherTable.ForginKey
INNER JOIN Shippers ON TableName.PrimeryKey = OtherTable.ForginKey;
```
