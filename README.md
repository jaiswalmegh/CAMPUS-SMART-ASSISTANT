📘 Smart Campus – Java Swing Student Management System

A complete Campus Smart Assistant / Student Management System built using Java Swing, JDBC, and MySQL.
This system allows admins to manage students, departments, faculty, courses, attendance, and more — with an easy-to-use graphical interface.

🚀 Features
🔹 Student Management

Add, update, view, and delete student records

Store admission number, name, course, department, contact info, etc.

🔹 Department Module

Add & manage different departments

Assign students to departments

🔹 Course Management

Add, edit, and delete course details

Map courses to departments

🔹 Attendance System

Mark daily attendance

View attendance per student

🔹 Faculty Module

Faculty registration & management

Department-wise faculty allocation

🔹 Admin Dashboard

GUI-based control panel

Navigation to all modules

🔹 Database Integration

Fully functional MySQL backend

Contains collegee.sql file for database setup

🗂️ Project Structure

Smart-Campus-main/
│── src/
│   ├── GUI/
│   │   ├── Main.java
│   │   ├── Student.java
│   │   ├── Courses.java
│   │   ├── Department.java
│   │   ├── Faculty.java
│   │   └── (other GUI forms)
│── collegee.sql
│── manifest.mf
│── build.xml
│── README.md


🛠️ Technologies Used

Java FX (GUI)

JDBC (Database connectivity)

MySQL

NetBeans / IntelliJ / Eclipse

OOP Concepts

SQL Relational Database

🗄️ Database Setup (MySQL)

Open phpMyAdmin / MySQL Workbench

Create a database:

🛠️ Technologies Used

Java Swing (GUI)

JDBC (Database connectivity)

MySQL

👤 Users Table

Stores login credentials and role information

CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    role ENUM('STUDENT', 'FACULTY', 'ADMIN') NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


🎓 Students Table

Stores academic and personal information of students.

CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    admission_no VARCHAR(30) UNIQUE NOT NULL,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    course VARCHAR(50),
    semester INT,
    year INT,
    FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE
);


NetBeans / IntelliJ / Eclipse

OOP Concepts

SQL Relational Database

🗄️ Database Setup (MySQL)

Open phpMyAdmin / MySQL Workbench

Create a database:

Import the collegee.sql file from the project.

Update JDBC connection details inside Java code if needed:

String url = "jdbc:mysql://localhost:3306/college";
String user = "root";
String pass = "your_password";


▶️ How to Run
Option 1: Using NetBeans (Recommended)

Open NetBeans

Click File > Open Project

Select the Smart-Campus-main folder

Run the project

Option 2: Using IntelliJ / Eclipse

Create a new Java project

Add all files from src/

Add MySQL JDBC driver to the classpath

Run Main.java
