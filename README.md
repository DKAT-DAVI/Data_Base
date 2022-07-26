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
***!=*** or ***<>*** Different \
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
***IN ()*** \
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

<h2><abbr title="Data Definition Language">DDL</abbr> COMMANDS</h2>

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

<h2><abbr title="Data Manipulation Language">DML</abbr> COMMANDS</h2>

## Insert values into table
~~~
INSERT INTO TableName (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
~~~
~~~
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
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

<h2><abbr title="Data Query Language">DQL</abbr> COMMANDS</h2>

## Select values
~~~
SELECT * FROM TableName;
~~~
~~~
SELECT column1, column2, ...
FROM TableName;
~~~

## Select Distinct
~~~
SELECT DISTINCT column1, column2, ...
FROM tableName;
~~~

## Ordered select
~~~
SELECT column1, column2, ...
FROM tableName
ORDER BY column1, column2, ...;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
ORDER BY column1, column2, ...
DESC;
~~~

## Select Where
~~~
SELECT column1, column2, ...
FROM tableName
WHERE conditions;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column = condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column != condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column > condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column < condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column >= condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column <= condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column IS NULL;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column IS NOT NULL;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 = condition AND column2 = condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 = condition OR column2 = condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 IN (condition);
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 NOT IN (condition);
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 BETWEEN condition1 AND condition2;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 IN (condition);
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 LIKE 'A';
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 LIKE '%A';
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 LIKE '%A%';
~~~
~~~
SELECT column1, column2, ...
FROM tableName
WHERE column1 LIKE '_A';
~~~

## Agregation Functions
~~~
SELECT COUNT(*) FROM tableName;
~~~
~~~
SELECT COUNT(column) FROM tableName;
~~~
~~~
SELECT MAX(column) FROM tableName;
~~~
~~~
SELECT MIN(column) FROM tableName;
~~~
~~~
SELECT AVG(column) FROM tableName;
~~~
~~~
SELECT SUM(column) FROM tableName;
~~~
## Group By
~~~
SELECT column1, column2, ...
FROM tableName
GROUP BY column;
~~~

## Having
~~~
SELECT column1, column2, ...
FROM tableName
GROUP BY columnName
HAVING condition;
~~~
~~~
SELECT column1, column2, ...
FROM tableName
GROUP BY columnName
HAVING colunm > (SELECT AVG(column) FROM tableName);
~~~