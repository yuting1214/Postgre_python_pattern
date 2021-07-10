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
- [Status](#status)
- [What's included](#whats-included)
- [Bugs and feature requests](#bugs-and-feature-requests)
- [Contributing](#contributing)
- [Creators](#creators)
- [Thanks](#thanks)
- [Copyright and license](#copyright-and-license)

## Connect To PostgreSQL Database Server
### Use psycopg2 as DB driver
To connect to the suppliers database, you use the **connect()** function of the **psycopg2** module.
The **connect()** function creates a new database session and returns a new instance of the connection class.
By using the connection object, you can create a new **cursor** to execute any SQL statements.
- [Code]()
