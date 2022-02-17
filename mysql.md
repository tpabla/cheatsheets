# MySQL
* [Reference Manual](https://dev.mysql.com/doc/refman/8.0/en/)

## Database operations
* Create a new database
  * `CREATE DATABASE {TEST};`
* Create a new user
  * `CREATE USER '{USERNAME}'@'{HOSTNAME}' IDENTIFIFED BY '{PASSWORD}';`
    * HOSTNAME can be `%` which means any host or `localhost` for local.
* Grant privileges to users for access to database.
  * `GRANT {PRIVILEGE} PRIVILEGES ON {DATABASE_NAME}.{TABLE_NAME} TO
    '{USERNAME}'@'{HOSTNAME}';`
    * [PRIVILEGE](https://dev.mysql.com/doc/refman/8.0/en/privileges-provided.html),
      typically `ALL`
* Commit changes
  * `FLUSH PRIVILEGES`
* Show all current users
  * `SELECT User,Host FROM mysql.user;`
* Show all current privileges
  * `SHOW GRANTS FORM '{USERNAME}'@'{HOSTNAME}';`
* Revoke privileges
  * `REVOKE {PRIVILEGE} ON {DATABASE_NAME}.{TABLE_NAME} FROM '{USERNAME}'@'{HOSTNAME};`
* Drop user
  * `DROP USER '{USERNAME}'@'{HOSTNAME}';`
