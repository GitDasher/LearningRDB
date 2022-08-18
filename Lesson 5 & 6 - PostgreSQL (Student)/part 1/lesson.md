# Lesson 5 & 6 - PostgreSQL (Student) Part 1

## Postgre Commands
- TRUNCATE <table_name>, <table_name>, ...., <table_name>; - Delete all the data from a table, must truncate every table that uses the required table entries as a foreign key

## Bash commands
- cat <file_name> - More but in one go
- <command_1> | <command_2> - | Pipe operator, pipe output from first command into second command, i.e. STDOUT of command 1 into STDIN of command 2
- IFS - Internal field seperator variable for bash, used to determine word boundaries, i.e. split regex
- PSQL="psql -X --username=<user_name> --dbname=<db_name> --no-align --tuples-only -c" - Create a variable for connecting to psql
- [[condition]] 
  - Flags
    - -z - Check if the condition is zero
- VARIABLE=$($PSQL "<query_>") - Store the query into the table and its result into a variable
- pg_dump --clean --create --inserts --username=<user_name> <database_name> > <file_name>.sql - Create a clean dump of database