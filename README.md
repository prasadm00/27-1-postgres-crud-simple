# 27-1-postgres-crud-simple


## Postgres setup

1. Go to posgres role
`$ sudo su - postgres`
`Enter password:`

`postgres@TTPL-LNV-0215:~$ psql postgres`

`postgres=# \conninfo`

2. Creating a role in Postgres
`postgres=# CREATE ROLE me WITH LOGIN PASSWORD 'password';`

3. We want me to be able to create a database:
`postgres=# ALTER ROLE me CREATEDB;`

4. You can run `\du` to list all roles and users:
    
5. Exit from the default session with `\q` for quit:

6. Now, we’ll connect postgres with me:

Use postgres user

1. create database
    `postgres=> CREATE DATABASE api;`
2. Use the `\list` command to see the available databases:
3. To connect with the database
   `postgres=> \c api`
    You are now connected to database "api" as user "me".
    `api=>`
4. Creating a table in Postgres
    `api=>
CREATE TABLE users (
  ID SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30)
);`
5. Insert into database
    `INSERT INTO users (name, email)
  VALUES ('Jerry', 'jerry@example.com'), ('George', 'george@example.com');`

6. see all users
    `api=> SELECT * FROM users;`
