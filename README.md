<h1 align="center"><u>MySQL</u></h1>
Learning about the SQL language 
Using MySQL and MySQL-Workbench

## MAIN PRIMITIVE TYPES
***BOOLEAN***
***INTEGER***
***DECIMAL(x,y)***
***FLOAT, REAL, DOUBLE***
***CHAR(n), VARCHAR(n)***
***TEXT(not-case)*** and ***BLOB(case)***
***DATE, TIME, DATETIME***

## CONSTRAINS
***NOT NULL***
***DEFAULT***
***UNIQUE***
***PRIMARY KEY***
***AUTO_INCREMENT***
***ENUM***
***IF EXISTS***
***IF NOT EXISTS***

## RELATIONAL OPERATORS

***=*** Equal \
***!=*** Different \
***>*** Major \
***<*** Minor \
***>=*** Greater equals \
***<=*** Less equal \
***is null*** Null field \
***is not null*** Field not null 

## LOGICAL OPERATORS

***AND*** \
***OR***  
***NOT***

## SPECIAL OPERATORS
***IN*** \
***BETWEEN***   
***LIKE*** \
***?***

## ARITHMETIC OPERATORS
***+*** Soma \
***-*** Subtração \
<b>*</b> Multiplicação \
***/*** Division \
***%*** Módulo \
***DIV*** Integer division 


## SQL FUNCTIONS
***Sqrt(x)*** Square root \
***pow(x,y)*** Potentiation \
***sin(x)*** Sine \
***Hex(x)*** Hexadecimal
[SQL FUNCTIONS](https://www.w3schools.com/sql/sql_ref_sqlserver.asp)

# MAIN SQL COMMANDS

## DDL COMMANDS

## Create a database

~~~
CREATE DATABASE DataBaseName;
~~~

## Use the data base
~~~
USE BancoDeDados;
~~~
## Create a table
~~~
CREATE TABLE TableName(
collum1 datatype restrictionList,
collum 2 datatype restrictionList,
collum 3 datatype restrictionList
);
 ~~~
 **Example:**
~~~
CREATE TABLE People(
name varchar(30),
age tinyint,
nationality varchar(30)
);
~~~

## Description of tables
~~~
DESC TableName;
~~~

## Delete an entire table
~~~
DROP TABLE TableName;
~~~

## Delete a entire database
~~~
DROP DATABASE DataBaseName;
~~~

## Add a column to a table
~~~
ALTER TABLE tableName
ADD COLUMN columnName dataType;
~~~
~~~
ALTER TABLE tableName
ADD COLUMN columnName dataType FIRST;
~~~
~~~
ALTER TABLE tableName
ADD COLUMN columnName dataType AFTER columnName;
~~~

## Delete column to table
~~~
ALTER TABLE tableName
DROP COLUMN columnName;
~~~

## Modify a column in a table
~~~
ALTER TABLE tableName
MODIFY COLUMN columnName dataType;
~~~

## Change column name
~~~
ALTER TABLE tableName
CHANGE COLUMN tableName newTableName dataType;
~~~

## Change table name
~~~
ALTER TABLE tableName
RENAME TO newTableName;
~~~

## Delete a table
~~~
DROP TABLE tableName;
~~~

## DML COMMANDS

## Insert values into table
~~~
INSERT INTO TableName (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
~~~
~~~
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
~~~

## Select values
~~~
SELECT column1, column2, ...
FROM TableName;
~~~
~~~
SELECT * FROM TableName;
~~~

## Update data in a table
~~~
UPDATE tableName
SET column1 =  value1, column2 = value2, ...
WHERE condition;
~~~

## Update data in a table with line limit
~~~
UPDATE tableName
SET column1 =  value1, column2 = value2, ...
WHERE condition
LIMIT numberOfLines;
~~~

## Delete data in a table
~~~
DELETE FROM tableName
WHERE condition
~~~

## Delete data in a table with line limit
~~~
DELETE FROM tableName
WHERE condition
LIMIT numberOfLines;
~~~

## Delete all data in a table
~~~
DELETE FROM tableName
~~~
~~~
TRUNCATE tableName
~~~