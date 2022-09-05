# SQL


# Select
```javascript
$$ Use To Get All Object In The Table 

//Select All Column 
SELECT * FROM users;

//Select Specific Column like Attribute In Sequlize
SELECT first_name, last_name FROM users;

//Create new Outpot For The Column
SELECT CONCAT(first_name, ' ', last_name) AS 'Name', dept FROM users;
```

# Where
```javascript
$$ Use To Get Specific Object In Table Where The property Match 

//Get The Data Where Have Specific Property
SELECT * FROM users WHERE location='Massachusetts';

//

```

