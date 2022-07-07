# MySQL
Aprendendo sobre a linguagem SQL <br>
Usando o MySQL e o SQL Workbench

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

## MATH FUCTIONS
***Sqrt(x)*** Square root \
***pow(x,y)*** Potentiation \
***sin(x)*** Sine \
***Hex(x)*** Hexadecimal

## SQL FUNCTIONS
<a href="https://www.w3schools.com/sql/sql_ref_sqlserver.asp">SQL FUNCTIONS</a>

# MAIN SQL COMMANDS

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

## Insert values into table
~~~
INSERT INTO TableName (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

INSERT INTO table_name
VALUES (value1, value2, value3, ...);
~~~

## Select values
~~~
SELECT column1, column2, ...
FROM TableName;

SELECT * FROM TableName;
~~~

## Delete an entire table
~~~
DROP TABLE TableName;
~~~

## Delete a entire database
~~~
DROP DATABASE DataBaseName;
~~~

