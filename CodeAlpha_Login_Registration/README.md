Task 2: Login and Registration System — C++

A simple C++ console-based Login and Registration System that allows users to create an account, store their credentials, and log in using their registered username and password.

This project was created as part of my CodeAlpha C++ Programming Internship.

Features
Allows users to register a new account
Takes username and password as input
Performs basic username validation
Performs basic password validation
Checks for duplicate usernames
Stores registered user credentials in a file
Allows registered users to log in
Verifies username and password during login
Displays appropriate success and error messages
Uses functions to organize registration and login operations
Uses file handling for persistent user data
Uses hashing before storing passwords
How the System Works

The program provides three main options:

Register
Login
Exit
Registration

When a user selects the registration option:

The program asks for a username.
The username is validated.
The program checks whether the username already exists.
The user enters a password.
The password is validated.
The password is hashed before being stored.
The username and hashed password are stored in a file.
Login

When a user selects the login option:

The program asks for the username.
The program asks for the password.
The entered password is hashed.
The program reads the stored credentials from the file.
The username and hashed password are compared.
A success message is displayed if the credentials match.
An error message is displayed if the credentials are invalid.
Validation

The program performs basic validation to ensure:

Username contains at least 3 characters
Username does not contain spaces
Password contains at least 6 characters
Duplicate usernames are not allowed

If invalid input is entered, the program displays an appropriate error message.

File Handling

The program uses a text file named:

users.txt

The file is used to store registered usernames and their hashed passwords.

The program uses:

ofstream — to write registered users to the file
ifstream — to read stored user credentials
ios::app — to add new users without overwriting existing users

The users.txt file is created automatically when the first user registers.

Technologies Used
C++
C++ Standard Library
iostream — input and output
fstream — file handling
string — storing usernames and passwords
functional — hashing passwords
Project Structure

CodeAlpha_Login_Registration/

│
├── main.cpp
└── README.md

During program execution, the following file is created:

users.txt

How to Run
Clone the repository

git clone <your-repository-url>

Open the project folder

cd CodeAlpha_Login_Registration

Compile the program

g++ main.cpp -o login_system

Run the program

Windows:
login_system

Linux/macOS:
./login_system

Sample Output
=====================================
LOGIN & REGISTRATION SYSTEM

----------- MENU -----------

Register
Login
Exit

Enter your choice: 1

========== REGISTRATION ==========
Enter username: Aryan
Enter password: 123456

Registration successful!
You can now login using your credentials.

Successful Login

----------- MENU -----------

Register
Login
Exit

Enter your choice: 2

========== LOGIN ==========
Enter username: Aryan
Enter password: 123456

Login successful!
Welcome, Aryan!

Duplicate Username

========== REGISTRATION ==========
Enter username: Aryan

Error: Username already exists.

Invalid Login

========== LOGIN ==========
Enter username: Aryan
Enter password: wrongpassword

Login failed!
Invalid username or password.

Concepts Used

This project demonstrates several fundamental C++ programming concepts:

Functions
Strings
File handling
ifstream
ofstream
Loops
Conditional statements
User input and output
Input validation
Hashing
Menu-driven programming
while loops
switch statements
C++ Standard Library functions
Input Validation

The program performs basic validation to ensure:

Username contains at least 3 characters
Username does not contain spaces
Password contains at least 6 characters
Username is not already registered

If invalid input is entered, the program displays an error message and returns to the main menu.

Security Consideration

The program hashes the password before storing it in the user file instead of directly storing the entered password.

This demonstrates the basic concept of avoiding plain-text password storage.

However, the std::hash function used in this educational project is not intended for production-grade password security. Real-world authentication systems should use dedicated password-hashing algorithms such as Argon2, bcrypt, or scrypt.

Future Improvements
Stronger password validation
Password confirmation during registration
Email-based registration
Password reset functionality
Multiple user roles such as Admin and User
Account lockout after multiple failed login attempts
Better password hashing using a dedicated password-hashing algorithm
Encryption for sensitive data
Database integration using MySQL or SQLite
Improved handling of invalid non-numeric input
Graphical user interface
User profile management
Learning Objective

The main objective of this project was to practice fundamental C++ programming concepts by building a practical authentication system.

Through this project, I practiced:

Working with functions
Taking and validating user input
Reading and writing files
Managing user credentials
Implementing registration and login logic
Checking for duplicate usernames
Working with strings
Using hashing
Organizing a menu-driven C++ application
Author

Aryan Srivastava

C++ Programming Internship — CodeAlpha

License

This project is created for educational and internship purposes.
