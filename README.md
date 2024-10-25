# Why does this exist <br>
- I was working on multiple projects that require a simple database, so why not work on an abstraction that can work on multiple projects. <br>

# When to use <br>
- You are a beginner in cplusplus who just wants something that works without concern for efficiency or build systems. <br>
- You you want a simple library that works while still in the ideation stage before you build or use something else more comprehensive / suitable for the project. <br>

# Features / Functions <br>
    vector <vector<string>> retrieveAllUserDataFromDatabaseForMatrix(const char * databaseFullPath, string tableName);

    int getTheNumbersOfColumnsInTable(const char * databaseFullPath, string tableName);

    int getTheNumbersOfRowsInTable(const char * databaseFullPath, string tableName);

    vector <vector<string>> retreiveDataWithMatchingValue(const char * databaseFullPath, string tableName, string id, string idValue) ;

    bool validateStringIsDigit(string value);

    template <typename T>
    bool isValidNumber(T value);

    template <typename T>
    double storeDataInDbUsingSingleTransaction(const char * databaseFullPath, string sqlInsertFormat, string sqlInsertTableNames, vector<vector <pair <T, string>>> matrixData);

    double storeDataInDbUsingSingleTransaction(const char * databaseFullPath, string sqlInsertFormat, string sqlInsertTableNames, vector<vector <pair <string, string>>> matrixData);

    double update(const char * databaseFullPath, string tableName, string columnName, string newColumnValue, string primaryKey, int keyValue);

    double deleteRow(const char * databaseFullPath, string tableName, string columnName, string primaryKey, int keyValue);

    double addNewColumn(const char * databaseFullPath, string tableName, string columnName, string sqliteDataType);

    double deleteColumn(const char * databaseFullPath, string tableName, string columnName);

    double storeSingleRowInDbUsingSingleInsert(const char * databaseFullPath, string sqlInsertFormat, string sqlInsertTableNames, string singleValueToInsert);

    double storeMultiRowsUsingConcatenatedInsertStmt(const char * databaseFullPath, string sqlInsertFormat, string sqlInsertTableNames, string singleValueToInsert);

    double deleteAllTableRows(const char * databaseFullPath, string tableName);
