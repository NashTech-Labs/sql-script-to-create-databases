# SQL Script To Create Database - SQL Server

This is a re-runnable SQL script which can create empty databases for you. You can copy and paste the given block as many times with a different database name to create those databases:

```aidl
use master;
IF DB_ID('ts_cm') IS NOT NULL
BEGIN
    ALTER DATABASE ts_cm
    SET SINGLE_USER
    WITH ROLLBACK IMMEDIATE;
    DROP DATABASE ts_cm
    CREATE DATABASE ts_cm
END
ELSE
BEGIN
    CREATE DATABASE ts_cm
END
```

## Note

This script will delete the existing database even if it is in use so use only to create fresh databases.