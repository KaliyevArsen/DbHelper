# Database Helper  

The Database Helper is a Python library that provides a set of methods for interacting with a SQLite database. The library is built around the sqlite3 library, which provides a simple interface for working with SQLite databases.


## Start

To use the Database Helper library, you first need to download library and create an instance of the Database class, passing in the name of the database file you want to connect to. Once you have created an instance of the Database class, you can use its methods to create tables, insert data, select data, update data, and delete data from the database.

<pre>
   pip install DbH
</pre>

<pre>
    from DbH import Database
    db = Database('example.db')
    db.create_table('users', [('id', 'INTEGER'), ('name', 'TEXT')
</pre>

## Methods

`create_table(table_name, columns)`: Creates a new table in the database with the specified name and columns. The columns parameter should be a list of tuples, where each tuple contains the name of a column and its data type.

`drop_table(table_name)`: Drops the specified table from the database.

`rename_table(old_name, new_name)`: Renames the specified table in the database.
add_column(table_name, column_name, data_type)`: Adds a new column to the specified table in the database.

`drop_column(table_name, column_name)`: Drops the specified column from the specified table in the database.

`rename_column(table_name, old_name, new_name)`: Renames the specified column in the specified table in the database.

`insert(table_name, data)`: Inserts a new row of data into the specified table in the database. The data parameter should be a dictionary containing the column names and their corresponding values.

`select_all(table_name)`: Retrieves all rows from the specified table in the database.

`select_where(table_name, condition)`: Retrieves all rows from the specified table in the database that meet the specified condition.

`update(table_name, data, condition)`: Updates the specified rows in the specified table in the database with the specified data. The data parameter should be a dictionary containing the column names and their corresponding values. The condition parameter should be a string representing the condition that the rows must meet.

`delete(table_name, condition)`: Deletes the specified rows from the specified table in the database. The condition parameter should be a string representing the condition that the rows must meet.

`count(table_name, condition=None)`: Returns the number of rows in the specified table in the database that meet the specified condition. If no condition is specified, the total number of rows in the table is returned.

`max(table_name, column)`: Returns the maximum value in the specified column of the specified table in the database.

`min(table_name, column)`: Returns the minimum value in the specified column of the specified table in the database.

`group_by(table_name, group_column)`: Groups the rows in the specified table in the database by the specified column, and returns the count of each group.

`join(table1, table2, join_column)`: Joins the specified tables in the database on the specified column, and returns the result.

`create_index(table_name, column)`: Creates an index on the specified column of the specified table in the database.

`close`: Closes the connection to the database.  


I hope this library will make your life easier <3
