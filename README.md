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
![](https://www.sqltutorial.org/wp-content/uploads/2016/03/SQL-INNER-JOIN.png)

## Inner Join 
##### The INNER JOIN keyword selects records that have matching values in both tables. 
```javascript
SELECT *
FROM Orders
INNER JOIN NameTable ON TableName.PrimeryKey = OtherTable.ForginKey
INNER JOIN Shippers ON TableName.PrimeryKey = OtherTable.ForginKey;
```
