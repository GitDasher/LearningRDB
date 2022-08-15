# Lesson 3 - PostgreSQL (Celestial)

## Terminal commands for saving and creating Postgre Databases
- Save database commands, pg_dump -cC --inserts -U <user_name> <database_name> > <file_name>.sql
- Create database using file, psql -U <root_user_postgres> < <file_name>.sql