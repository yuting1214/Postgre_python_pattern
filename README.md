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
1. First conntect to the database server
```
conn = psycopg2.connect(dsn)
```
The connect() function returns a new instance of the connection class.

2. Create a new cursor object by calling the cursor() method of the connection object.
```
cur = conn.cursor()
```
3. You pass the INSERT statement to the first parameter and a list of values to the second parameter of the execute() method.
```
cur.execute(sql, (value1,value2))
```
4. (Optional) If there is a primary key in table, you can get the generated ID back after inserting the row.
```
id = cur.fetchone()[0]
```
5. After that, call the commit() method of the connection object to permanently save the changes to the database.
```
conn.commit()
```
If you forget to call the commit() method, psycopg2 will not make any changes to the table.

6. Finally, close the connection to the PostgreSQL database server by calling the close() method of the cursor and connection objects.
```
cur.close()
conn.close()
```

- [Code](https://github.com/yuting1214/Postgre_python_pattern/blob/master/code/create_table.md)
