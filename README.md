# Database Abstraction Library
This is a lightweight C++ library that provides a simplified interface for performing common database operations using SQLite. With this library, you can interact with SQLite databases, retrieve data, validate input, and perform basic CRUD operations.

# Why does this exist
- I was working on multiple projects that require a simple database, so why not work on an abstraction that can work on multiple projects.

# When to use
- You are a beginner in C++ who just wants something that works without concern for efficiency or build systems.
- You want a simple library that works while still in the ideation stage before you build or use something else more comprehensive/suitable for the project.

# Features
- Retrieve data from tables in matrix form
- Insert, update, and delete rows and columns
- Validate numeric data types
- Use transactions for efficient data insertion
- Easy integration with SQLite databases

# Dependencies
- **SQLite3**: Ensure you have the SQLite3 library installed and available.

# Key Functions
1. **Data Retrieval**
   - **Retrieve All Data as Matrix**  
     Fetches all data from a specified table.  
     ```cpp
     vector<vector<string>> data = databaseAbstraction::retrieveAllUserDataFromDatabaseForMatrix("database_path", "table_name");
     ```

   - **Retrieve Data by Matching Value**  
     Retrieves rows with a specific column value.  
     ```cpp
     vector<vector<string>> data = databaseAbstraction::retreiveDataWithMatchingValue("database_path", "table_name", "column_id", "value");
     ```

2. **Table Information**
   - **Get Column Count**  
     Returns the number of columns in a table.  
     ```cpp
     int columnCount = databaseAbstraction::getTheNumbersOfColumnsInTable("database_path", "table_name");
     ```

   - **Get Row Count**  
     Returns the number of rows in a table.  
     ```cpp
     int rowCount = databaseAbstraction::getTheNumbersOfRowsInTable("database_path", "table_name");
     ```

3. **Data Manipulation**
   - **Insert Data with Transaction**  
     Stores data in a table using a transaction for efficiency.  
     ```cpp
     double result = databaseAbstraction::storeDataInDbUsingSingleTransaction("database_path", "INSERT INTO table", "table_name", matrix_data);
     ```

   - **Single Row Insert**  
     Stores a single row of data.  
     ```cpp
     double result = databaseAbstraction::storeSingleRowInDbUsingSingleInsert("database_path", "INSERT INTO table", "table_name", "value_to_insert");
     ```

   - **Store Multiple Rows with Concatenated Insert**  
     Stores multiple rows in a single insert statement.  
     ```cpp
     double result = databaseAbstraction::storeMultiRowsUsingConcatenatedInsertStmt("database_path", "INSERT INTO table", "table_name", "value_to_insert");
     ```

   - **Update Row**  
     Updates a specific row in the table.  
     ```cpp
     double result = databaseAbstraction::update("database_path", "table_name", "column_name", "new_value", "primary_key", key_value);
     ```

   - **Delete Row**  
     Deletes a row based on the primary key.  
     ```cpp
     double result = databaseAbstraction::deleteRow("database_path", "table_name", "column_name", "primary_key", key_value);
     ```

   - **Delete All Rows in Table**  
     Deletes all rows from a specified table.  
     ```cpp
     double result = databaseAbstraction::deleteAllTableRows("database_path", "table_name");
     ```

4. **Column Manipulation**
   - **Add New Column**  
     Adds a new column to the table.  
     ```cpp
     double result = databaseAbstraction::addNewColumn("database_path", "table_name", "column_name", "SQLITE_DATATYPE");
     ```

   - **Delete Column**  
     Removes a column from the table.  
     ```cpp
     double result = databaseAbstraction::deleteColumn("database_path", "table_name", "column_name");
    ```

