# MySQL notes
My sql is case-insensitive language

## My sql commands

 - Delete the whole database
 ```
 DROP DATABASE 
 ```

 - List all databases
```
SHOW TABLES
```

 - Create Table
 ``` 
 CREATE TABLE <NAME> (<ATTRIBUTE_1_NAME> <ATTRIBUTE_1_TYPE, <ATTRIBUTE_2_NAME> <ATTRIBUTE_3_TYPE ...>) 
 ```

 - Drop tables
```
DROP TABLE <TABLE_NAME>
```

 - Get details about a table and its attributes
``` 
DESCRIBE <TABLE_NAME>
```

### Data Types
- Numeric: `INT, DECIMAL, BIGINT`, etc
- String: `CHAR, VARCHAR, ENUM`, etc
- Datetime: `DATE, TIME, DATETIME`
- `JSON`

- Select
``` 
SELECT * FROM <TABLE_NAME> WHERE <CONDITION> 
```

- Operators
```
> , < , >= , <= , != , <>(not equals) , =(equals) , IN , LIKE, etc 
```

- Like
```
SELECT COL1, COL2, .. FROM <TABLE_NAME> WHERE <TARGET_COLUMN_TO_PERFORM_CONDITION_ON> LIKE "STRING" 
```

here, string can be of the following forms:

`"%str"`: matches suffix (strings ending with 'str')

`"str%"`: matches prefix (strings starting with 'str')

`"%str%"`: finds values having 'str' in any position

`"_s"`: values having s in the second position

`"s_"`: values having second last substring 's'

`"a%b"`: starts with a and ends with b

- Combining Query filters:
``` 
SELECT * FROM ACTORS WHERE CHARGES >=35000 AND ID<4
```
queries can be combined using `AND, OR, NOT`

- OrderBy
```
select col1, col2 ... from <table_name> ORDERBY <colA> <asc or desc>, <colB> <asc or desc>;
```
if two entries in colA have same values then it orders by the colB in their respective orders defined.

- Limit: used to show a smaller chunk of the record
```
select col1, col2 ... from <table_name> LIMIT 5 OFFSET 2;
```
the above query divides the records into chunks of 5 each and fetches the third (0-based) chunk using offset query.
```

- 