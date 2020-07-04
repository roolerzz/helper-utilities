<h3>Postgres-helper</h3>
Contains helper functions and notes for dealing with postgres.


<h4>Commands</h4>

- `SHOW ALL`
- `SHOW DEFAULT_TRANSACTION_ISOLATION`. Btw default on postgres is `READ COMMITTED`.


<h4>PSQL Commands</h4>

- `\l` - Show all the databases in the current server.
- `\dt` - Show tables in the current database. Alternate:
```SQL
SELECT * FROM pg_catalog.pg_tables WHERE 	schemaname != 'pg_catalog' AND schemaname != 'information_schema';
```

- `\d TABLE_NAME` - Describes a specified table. Alternate:
  ```SQL
  SELECT * FROM information_schema.COLUMNS WHERE TABLE_NAME = 'city';
  ```
- `psql -d DATABASE_NAME -U  USER_NAME -W` - Connects to a specified DATABASE_NAME with a specified USER_NAME and promts for password.
- 
