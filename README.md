<p align="center">
  <a href="https://example.com/">
    <img src="https://via.placeholder.com/72" alt="Logo" width=72 height=72>
  </a>

  <h3 align="center">Logo</h3>

  <p align="center">
    Short description
    <br>
    <a href="https://reponame/issues/new?template=bug.md">Report bug</a>
    ·
    <a href="https://reponame/issues/new?template=feature.md&labels=feature">Request feature</a>
  </p>
</p>


## Table of contents

- [Connect To PostgreSQL Database Server](#connect-to-postgresql-database-server)
- [Create Tables](#create-tables)
- [Insert data into PostgreSQL](#insert-data-into-postgresql)
- [Bugs and feature requests](#bugs-and-feature-requests)
- [Contributing](#contributing)

## Connect To PostgreSQL Database Server
### Use psycopg2 as DB driver
To connect to the suppliers database, you use the **connect()** function of the **psycopg2** module.
The **connect()** function creates a new database session and returns a new instance of the connection class.
By using the connection object, you can create a new **cursor** to execute any SQL statements.

- [Code](https://github.com/yuting1214/Postgre_python_pattern/blob/master/code/connect.md)

## Create Tables
To create a new table in a PostgreSQL database, you use the following steps:

1. First, construct **CREATE TABLE** statements.
2. Next, connect to the PostgreSQL database by calling the **connect()** function. The **connect()** function returns a connection object.
3. Then, create a cursor object by calling the **cursor()** method of the connection object.
4. After that, execute the **CREATE TABLE** by calling the **execute()** method of the **cursor** object.
5. Finally, close the communication with the PostgreSQL database server by calling the **close()** methods of the cursor and connection objects.

- [Code](https://github.com/yuting1214/Postgre_python_pattern/blob/master/code/create_table.md)

## Insert data into PostgreSQL
