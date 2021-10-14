
## How to import CSV files that contain mm/dd/yyyy into MariaDB (using HeidiSQL)?
```sql
-- convert data type of column to VARCHAR (which allows you to import the dates as mm/dd/yyyy without causing an error
ALTER TABLE `[table_name]` CHANGE COLUMN `[column_name]` `[column_name]` VARCHAR(20) NULL DEFAULT NULL AFTER `[column_prior_to_the_column_you_want_to_change]`;

-- import CSV file <--

-- change the format of mm/dd/yyyy -> yyyy-mm-dd
UPDATE [table_name] SET [column_name]=CONCAT_WS('-', SUBSTR([column_name], 7, 4), SUBSTR([column_name], 1, 2), SUBSTR([column_name], 4, 2));

-- this changes the data type of the date column to the DATE data type
ALTER TABLE `[table_name]` CHANGE COLUMN `[column_name]` `[column_name]` DATE NULL DEFAULT NULL AFTER `[column_prior_to_the_column_you_want_to_change]`;

```


