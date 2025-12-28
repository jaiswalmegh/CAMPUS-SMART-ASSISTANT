# 🎓 Smart Campus Management System

A Java Swing–based desktop application designed to manage academic entities such as **Students, Courses, Departments, and Instructors** using a centralized database.

This project is suitable for academic submission and demonstrates clean UI design, modular structure, and database connectivity.

---

## 📌 Project Overview

The **Smart Campus Management System** is a desktop-based application built using **Java Swing** and **JDBC**.  
It provides a user-friendly interface to manage institutional data efficiently.

---

## 🧩 Modules Included

### ✅ Main Dashboard
- Acts as the central navigation screen  
- Sidebar-based layout  
- Opens all functional modules  

### ✅ Student Module
- Add student records  
- View student details  
- Delete records  
- Connected to database  
- Displayed in tabular format  

### ✅ Course Module
- Add new courses  
- View course list  
- Delete course records  

### ✅ Department Module
- Manage department details  
- Add / view / delete departments  

### ✅ Instructor Module
- Manage instructor information  
- Assign department  
- View instructor records  

---

## 🛠️ Technologies Used

- Java (JDK 8 or higher)
- Java Swing (GUI)
- JDBC
- SQL Server
- NetBeans / IntelliJ IDEA
- MVC-style separation

---

## 🗂️ Project Structure

```
Smart-Campus/
│
├── src/
│   └── GUI/
│       ├── Main.java
│       ├── StudentPanel.java
│       ├── CoursePanel.java
│       ├── DepartmentPanel.java
│       ├── InstructorPanel.java
│       │
│       ├── Student.java              (legacy DB logic)
│       ├── Courses.java
│       ├── Department.java
│       ├── Instructor.java
│       │
│       ├── DBConnection.java
│       ├── StudentDAO.java
│       ├── CourseDAO.java
│       ├── DepartmentDAO.java
│       └── InstructorDAO.java
│
└── README.md
```

---

## 🗄️ Database Configuration

Update database credentials inside:

```
DBConnection.java
```

Example configuration:

```java
jdbc:sqlserver://localhost:1433;databaseName=collegee
```

```java
username = sa
password = your_password
```

---

## 📋 Suggested Database Tables

### Student Table
```sql
CREATE TABLE student (
    id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100),
    department VARCHAR(100),
    phone VARCHAR(15)
);
```

### Course Table
```sql
CREATE TABLE course (
    id VARCHAR(20),
    name VARCHAR(100),
    credits VARCHAR(10),
    department VARCHAR(100)
);
```

### Department Table
```sql
CREATE TABLE department (
    id VARCHAR(20),
    name VARCHAR(100)
);
```

### Instructor Table
```sql
CREATE TABLE instructor (
    id VARCHAR(20),
    name VARCHAR(100),
    department VARCHAR(100),
    phone VARCHAR(15)
);
```

---

## ▶️ How to Run the Project

### Option 1: Using an IDE (Recommended)
1. Open the project in **NetBeans / IntelliJ IDEA**
2. Configure JDK
3. Ensure SQL Server is running
4. Update database credentials
5. Run:
```
Main.java
```

### Option 2: Command Line
```bash
javac GUI/*.java
java GUI.Main
```

---

## 🎨 UI Features

- Dark themed interface
- Sidebar navigation
- Clean dashboard layout
- Table-based data views
- Modular and extendable design
- User-friendly workflow

---

## 🚀 Future Enhancements

- Login & authentication system
- Role-based access (Admin / Faculty)
- Search & filter functionality
- Edit/update records
- Report generation
- Charts & analytics
- AI-based assistant
- Export to PDF / Excel
- Theme switching

---

## 📘 Academic Usage

This project is suitable for:
- Java Mini Projects
- DBMS + Java integration assignments
- College practical submissions
- UI/UX enhancement demos
- Final-year project base

---

## 👨‍💻 Author

Developed as part of an academic **Smart Campus Management System** project using Java Swing and SQL Server.

---

✅ You may freely extend, modify, or customize this project for learning or academic purposes.
