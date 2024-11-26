 Employee Management System

This project consists of two interconnected modules:  

1. Java Application** for performing CRUD operations on employee data stored in a relational database using JDBC.  
2. JavaFX Application** to manage and display a list of employees and their salaries, utilizing an abstract class to represent different employee types.  

---

 Project Overview

 1. Java Module: Database Operations with JDBC

Features:

- Database Setup:
  - A database called `employee_db` containing a table `employee` with the following schema:
    - `id` (integer, primary key, auto-increment).
    - `name` (string, representing the employee's name).
    - `position` (string, indicating job title).
    - `salary` (decimal, reflecting the employee's pay).
    - `hire_date` (date, showing when the employee was hired).

- Entity Class:
  - A class `Employee` models the employee data with fields:
    - `id`, `name`, `position`, `salary`, and `hireDate`.
  - Includes a constructor, getter and setter methods, and a `toString()` implementation for representing employee details as a string.

- Data Access Class:
  - The `EmployeeData` class handles database interactions via JDBC, with methods such as:
    - `createEmployee(Employee employee)`: Inserts a new employee record.
    - `getEmployeeById(int id)`: Fetches a single employee using their ID.
    - `getAllEmployees()`: Retrieves all employee records.
    - `updateEmployee(Employee employee)`: Modifies an existing employee's details.
    - `deleteEmployee(int id)`: Removes an employee by their ID.
  - Additionally, it provides methods to establish and manage database connections.

- Testing and Demonstration:
  - A `main()` method showcases the functionality:
    - Adding a new employee.
    - Fetching and displaying an employee by their ID.
    - Listing all employees.
    - Updating employee details.
    - Deleting an employee record.

---

2. JavaFX Module: Employee Salary Management System

Features:

- Abstract Class Structure:
  - The `Employee` abstract class includes a method `calculateSalary()` that is implemented in its subclasses:
    - FullTimeEmployee: Computes an annual fixed salary.
    - PartTimeEmployee: Calculates wages based on hours worked and hourly rate.
    - Contractor: Determines earnings using an hourly rate and maximum allowable hours.

- Graphical User Interface (GUI):
  - TableView:
    - Displays a list of employees with details such as:
      - Name, Employee Type, and Calculated Salary.
  - Input Fields:
    - Fields for adding employee data:
      - Name and Type (selectable options: Full-time, Part-time, Contractor).
      - Additional fields for Part-time and Contractor:
        - Hours Worked (Part-time) and Maximum Hours (Contractor), along with Hourly Rate.
  - Buttons:
    - Add Employee: Adds a new employee to the table.
    - Calculate Salaries: Recalculates and updates the salary column.
    - Remove Employee: Deletes the selected employee from the table.

- Validation Mechanism:
  - Ensures correct input, such as enforcing positive numbers for hours and rates.

---

Getting Started  

Prerequisites:
- Java Development Kit (JDK) 
- JavaFX SDK.
- Relational Database (e.g., MySQL or PostgreSQL).
- JDBC Driver

Setup Guide:  

1. Database Setup:
   - Create the database:
     ```sql
     CREATE DATABASE employee_db;
     USE employee_db;

     CREATE TABLE employee (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(100),
         position VARCHAR(100),
         salary DOUBLE,
         hire_date DATE
     );
     ```
   - Update the database connection details (JDBC URL, username, and password) in the `EmployeeData` class.

2. JavaFX Setup:
   - Add the JavaFX library to your project.
   - Run the JavaFX application to access the GUI for managing employees and their salaries.

This system provides a comprehensive solution for managing employee information both in the database and in a user-friendly graphical interface.
![Описание изображения](путь/к/изображению)




