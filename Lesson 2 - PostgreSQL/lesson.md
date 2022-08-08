# Lesson 2 - PostgreSQL

## Postgre commands
- psql -U <user_name> : Log into PostgreSQL with username <user_name>
  - or psql --username=<user_name> dbname=<db_name>
- \l - List all databases
- CREATE DATABASE <database_name>; : Create a database under the name <database_name>, semi-colon is a must
- \c <database_name> : Connect to the database under the name <database_name>
- \d : Display all the tables in the current database
- CREATE TABLE <table_name>(); : Create a table under the name <table_name> in the current database;
- ALTER TABLE <table_name> ADD COLUMN <column_name> DATATYPE; : Alter the table <table_name> to add a column under the name <column_name> with the given datatype
  - Datatypes
    - INT : Integer
    - VARCHAR(number) : Variable Characters (Character Varying) of length number
    - 
- ALTER TABLE <table_name> DROP COLUMN <column_name>; : Alter the table <table_name> to drop the column with the name <column_name>
- ALTER TABLE <table_name> RENAME COLUMN <column_name> TO <new_name>; : Alter the table <table_name> to change the name of the column <column_name> to <new_name>
- INSERT INTO <table_name(column 1, column 2)> VALUES(<values 1, values 2>); : Insert <values 1, values 2> into <column 1, column 2> of <table_name> respectively
  - Datatypes
    - INT : 1, 2, 3, etc.
    - VARCHAR : 'Samus', 'Alexa', 'Siri' etc.
- 