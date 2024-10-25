# Database Abstraction Library
This is a lightweight C++ library that provides a simplified interface for performing common database operations using SQLite. With this library, you can interact with SQLite databases, retrieve data, validate input, and perform basic CRUD operations.



# Why does this exist <br>
- I was working on multiple projects that require a simple database, so why not work on an abstraction that can work on multiple projects. <br>

# When to use <br>
- You are a beginner in cplusplus who just wants something that works without concern for efficiency or build systems. <br>
- You you want a simple library that works while still in the ideation stage before you build or use something else more comprehensive / suitable for the project. <br>

# Features<br>
- Retrieve data from tables in matrix form <br>
- Insert, update, and delete rows and columns <br>
- Validate numeric data types <br>
- Use transactions for efficient data insertion <br>
- Easy integration with SQLite databases <br>

Dependencies
- SQLite3: Ensure you have the SQLite3 library installed and available.<br>

# Key Functions <br>
1. Data Retrieval
  - Retrieve All Data as Matrix <b>
    Fetches all data from a specified table.<br>
    `vector<vector<string>> data = databaseAbstraction::retrieveAllUserDataFromDatabaseForMatrix("database_path", "table_name");`
