# University Management System 🎓

A C++ console-based application integrated with MySQL for managing student records. The system allows users to perform basic CRUD (Create, Read, Update, Delete) operations on student data, including inserting, displaying, searching, updating, and deleting records.

## Features ✨

- **Insert Student Data**: Add new student records with details like ID, Name, Subject, and CGPA.
- **Display All Students**: View all student records stored in the MySQL database.
- **Search Student Data**: Look up a student by their ID and display their information.
- **Update Student Information**: Modify a student's subject based on their ID.
- **Delete Student Data**: Remove a student's record from the database by their ID.

## Technologies Used 🛠️

- **C++**: Core logic and implementation of the University Management System.
- **MySQL**: Database management system to store and retrieve student records.
- **MySQL C API**: Used to connect the C++ application with the MySQL database.

## Setup and Installation ⚙️

1. **Install MySQL**:
   - Make sure MySQL is installed and running on your system. Create a database named `mydb` and a table called `student` with the following structure:

   ```sql
   CREATE DATABASE mydb;
   USE mydb;

   CREATE TABLE student (
       Id INT PRIMARY KEY,
       Name VARCHAR(100),
       Subject VARCHAR(100),
       CGPA FLOAT
   );
2. **Configure the Project:**:
   - Replace the MySQL connection details (HOST, USER, PW, DB) in the code with your own       
     credentials:
       ```sql
       const char* HOST = "localhost";
      const char* USER = "root";
      const char* PW = "your password";
      const char* DB = "mydb";
3. **Compile and Run:**:
   - Compile the C++ code using any C++ compiler (e.g., g++, Visual Studio).
   - Make sure to link the MySQL library during compilation
    ```sql
   g++ -o university_management_system university_management_system.cpp -lmysqlclient
4. ** Run the program :**:
   - After compiling, run the program
       ```sql
      ./university_management_system
