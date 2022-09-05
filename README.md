# SQL


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

