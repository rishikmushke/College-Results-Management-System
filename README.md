Student Management System

Description

A console-based Student Management System developed using C programming. The project provides separate login systems for faculty and students and offers different dashboards based on the type of user.

The system is designed to manage and display student academic information, internal marks, examination results, placement information, library information, and college notifications.

Features

Faculty Login

- Faculty authentication using username and password
- Faculty dashboard
- View student details
- View Internal Marks 1
- View Internal Marks 2
- View college notifications
- Logout option

Student Login

- Student authentication using username and password
- Student dashboard
- Academic section
- Examination cell
- View semester results
- Calculate CGPA
- Pass/Fail status
- Library information
- Placement information
- College notifications
- Exit option

Modules

1. Faculty Login
2. Student Login
3. Student Details
4. Internal Marks
5. Examination Cell
6. CGPA Calculation
7. Library
8. Placements
9. Notifications

Technologies Used

- C Programming
- GCC / C Compiler

C Programming Concepts Used

- Structures
- Array of Structures
- Strings
- "strcmp()"
- Loops
- Conditional Statements
- "switch" Statements
- Functions from Standard Libraries
- User Input and Output
- Basic Arithmetic Operations

Structures Used

Faculty Structure

The "struct id" structure stores faculty information such as:

- Faculty ID
- Faculty name
- Department
- Username
- Password

Student Structure

The "struct rollno" structure stores student information such as:

- Username
- Password
- Hall Ticket Number
- Student Name
- Branch
- Internal Marks
- Semester SGPA

Placement Structure

The "struct year" structure stores placement-related information such as:

- Student name
- Package

Login System

The program provides two login options:

1. Faculty Login
2. Student Login

After successful authentication, the user is redirected to the corresponding dashboard.

Faculty Dashboard

--- FACULTY DASHBOARD ---

1. STUDENT DETAILS
2. INTERNAL MARKS
3. NOTIFICATION
4. LOGOUT

Student Dashboard

--- DASHBOARD ---

1. ACADEMICS
2. EXAMINATION CELL
3. LIBRARY
4. PLACEMENTS
5. NOTIFICATION
6. EXIT

Examination Module

The examination section allows students to check their semester results.

The system displays:

- Roll Number
- Name
- Branch
- SGPA
- CGPA
- Pass/Fail status

For Semester 2, the CGPA is calculated using the available semester SGPA values.

Placement Module

The placement section displays a list of students and their packages.

Example:

NAME            PACKAGE

rishik          16 LPA
ravi            7 LPA
koushik         18 LPA
gitesh          6 LPA
Sujith          20 LPA

Library Module

The system provides basic information about the central library and encourages students to use books and learning resources.

Notification Module

The notification section displays college-related announcements available in the program.

How to Run

1. Download or clone this repository.
2. Open the ".c" source file in a C compiler.
3. Compile the program using GCC or another C compiler.
4. Run the generated executable.
5. Select Faculty Login or Student Login.
6. Enter the required credentials.
7. Navigate through the dashboard using the available options.

Project Objective

The main objective of this project is to develop a simple college management application using C programming while applying concepts such as structures, arrays, strings, loops, conditional statements, and switch-case statements.

Future Improvements

- Add file handling for permanent data storage
- Add student registration
- Add faculty registration
- Add password change functionality
- Add more semester results
- Add complete academic information
- Add attendance management
- Add fee management
- Add a graphical user interface
- Connect the system to a database

Author
Mushke Rishik
Language: C
