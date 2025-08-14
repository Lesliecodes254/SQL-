# Database Operations - SQL Queries

This repository contains basic SQL queries for database management operations.

## Overview

The SQL scripts in this project demonstrate fundamental database operations:
- Creating a new database
- Dropping (deleting) an existing database

## Files

### `database_queries.sql`
Contains two essential database management queries:
1. **Database Creation**: Creates a new database called `salesDB`
2. **Database Deletion**: Drops an existing database called `demo`

## SQL Commands

### 1. Create Database
```sql
CREATE DATABASE salesDB;
```
**Purpose**: Creates a new database named "salesDB"

**Use Case**: Initialize a new database for sales-related data storage

### 2. Drop Database
```sql
DROP DATABASE demo;
```
**Purpose**: Permanently deletes the database named "demo" and all its contents

**Use Case**: Remove unused or test databases

## Prerequisites

- SQL database management system (MySQL, PostgreSQL, SQL Server, etc.)
- Database user with appropriate privileges:
  - `CREATE` privilege for creating databases
  - `DROP` privilege for deleting databases
- Database connection/client tool (MySQL Workbench, pgAdmin, SQL Server Management Studio, etc.)

## Usage Instructions

1. **Connect to your database server** using your preferred SQL client
2. **Execute the queries** one at a time or as needed
3. **Verify the operations** by checking your database list

### Running the Queries

```sql
-- To create the salesDB database
CREATE DATABASE salesDB;

-- To drop the demo database (use with caution)
DROP DATABASE demo;
```

## Important Warnings

⚠️ **CRITICAL**: The `DROP DATABASE` command is **irreversible** and will permanently delete:
- All tables in the database
- All data stored in those tables
- All database objects (views, procedures, functions, etc.)
- All user permissions specific to that database

### Best Practices

1. **Backup First**: Always create a backup before dropping a database
2. **Double-Check**: Verify you're targeting the correct database
3. **Use IF EXISTS**: Consider using safer syntax when available:
   ```sql
   DROP DATABASE IF EXISTS demo;
   ```
4. **Test Environment**: Practice these commands in a test environment first

## Database System Compatibility

These queries are compatible with most SQL database systems:
- ✅ MySQL
- ✅ PostgreSQL
- ✅ SQL Server
- ✅ Oracle
- ✅ SQLite (with limitations)
- ✅ MariaDB

## Error Handling

Common errors you might encounter:

| Error | Cause | Solution |
|-------|-------|----------|
| Access denied | Insufficient privileges | Contact your DBA for appropriate permissions |
| Database exists | Database already created | Use `CREATE DATABASE IF NOT EXISTS` |
| Database not found | Trying to drop non-existent DB | Use `DROP DATABASE IF EXISTS` |

## Security Considerations

- Only run these commands with appropriate authorization
- Use principle of least privilege - only grant necessary permissions
- Monitor database operations in production environments
- Implement proper backup and recovery procedures

## Contributing

When adding new database operations:
1. Follow SQL standard naming conventions
2. Include appropriate comments
3. Update this README with new commands
4. Test queries across different database systems

## License

This code is provided as-is for educational and development purposes.

---

**Last Updated**: August 2025  
**Author**: Database Administrator  
**Version**: 1.0
