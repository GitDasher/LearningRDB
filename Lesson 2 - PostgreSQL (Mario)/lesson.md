# Lesson 2 - PostgreSQL (Mario)

## Postgre commands
- psql -U <user_name> : Log into PostgreSQL with username <user_name>
  - or psql --username=<user_name> dbname=<db_name>
- \l - List all databases
- CREATE DATABASE <database_name>; : Create a database under the name <database_name>, semi-colon is a must
- \c <database_name> : Connect to the database under the name <database_name>
- \d : Display all the tables in the current database
- \d <table_name> : Display the <table_name>'s details
- CREATE TABLE <table_name>(); : Create a table under the name <table_name> in the current database;
- ALTER TABLE <table_name> ADD COLUMN <column_name> <datatype> <constraint>; : Alter the table <table_name> to add a column under the name <column_name> with the given datatype
  - Datatypes
    - INT : Integer
    - VARCHAR(number) : Variable Characters (Character Varying) of length number
    - Serial : Not null integers serialised
    - NUMERIC(number, precision) : Number of digits is number with precision amount to the right of the decimal
    - BOOLEAN : True or False
    - TEXT : Used to store text of infinite length
  - Constraints
    - NOT NULL : Can't be empty
    - 
- ALTER TABLE <table_name> DROP COLUMN <column_name>; : Alter the table <table_name> to drop the column with the name <column_name>
- ALTER TABLE <table_name> RENAME COLUMN <column_name> TO <new_name>; : Alter the table <table_name> to change the name of the column <column_name> to <new_name>
- INSERT INTO <table_name(column 1, column 2)> VALUES(<values 1, values 2>); : Insert <values 1, values 2> into <column 1, column 2> of <table_name> respectively
  - Datatypes
    - INT : 1, 2, 3, etc.
    - VARCHAR : 'Samus', 'Alexa', 'Siri' etc.
- SELECT <columns> FROM <table_name> ORDER BY <column>; : Show data from <columns> of <table_name> sorted using <column> data
- DELETE FROM <table_name> WHERE <condition>; : Delete row from <table_name> where <condition> is met
- ALTER DATABASE <database_name> RENAME TO <new_database_name>; : Change the name of <database_name> to <new_database_name>
- UPDATE <table_name> SET <column_name>=<new_value> WHERE <condition>; : Update the table entry <column_name> of <table_name> to <new_value> where <condition> is met
- ALTER TABLE <table_name> ADD PRIMARY KEY(<column_name>); : Make <column_name> of <table_name> a primary key
- ALTER TABLE <table_name> DROP CONSTRAINT <constraint_name>; : Remove the constraint <constraint_name> from <table_name> (Constraints show up under indexes when \d <table_name> is used)
- ALTER TABLE <table_name> ADD COLUMN <column_name> <datatype> <constraints> REFERENCES <referenced_table_name>(<referenced_column_name>); : Alter table <table_name> to add a foreign key <column_name> with <datatype> that references <referenced_column_name> from <referenced_table_name> with <constraints>
- ALTER TABLE <table_name> ADD UNIQUE(<column_name>); : Alter the table <table_name> to add a unique key to <column_name> to have a 'one-to-one' relationship
- ALTER TABLE <table_name> ALTER COLUMN <column_name> SET <constraint>; : Alter the table <table_name> to add a constraint to a column <column_name>
- CREATE TABLE <table_name>(<column_name> <data_type> <constraints_>); : Create a table under the name <table_name> with <column_name> having <data_type> and <constrains_> 
- ALTER TABLE <table_name> ADD FOREIGN KEY(<column_name>) REFERENCES <referenced_table>(<referenced_column>); : Alter table <table_name> to add a foreign key to <column_name> which references <referenced_column> of <referenced_table>
- ALTER TABLE <table_name> ADD PRIMARY KEY(<column1>, <column2>); : Alter table <table_name> to create a composite key, using <column1> and <column2>
- SELECT <columns> FROM <table_1> FULL JOIN <table_2> ON <table_1.primary_key_column> = <table_2.foreign_key_column>; : Select <columns> from <table_1> while joining them with <table_2> using keys <table_1.primary_key_column> and <table_2.foreign_key_column>. A Join is used to establish a connection
- SELECT <columns> FROM <junction_table>
FULL JOIN <table_1> ON <junction_table.foreign_key_column> = <table_1.primary_key_column>
FULL JOIN <table_2> ON <junction_table.foreign_key_column> = <table_2.primary_key_column>; : Join multiple tables
- () For Alter is a must
