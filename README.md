
# 🏨 Hostel Management Database | DBMS

A relational **Hostel Management Database System** developed as a Database Management Systems (DBMS) project. The system is designed to efficiently manage hostel operations including students, rooms, beds, allocations, payments, complaints, staff, and maintenance requests.

## 📌 Project Overview

Managing hostel information manually can lead to data duplication, inconsistencies, and difficulties in tracking student allocations, payments, complaints, and maintenance activities.

This project implements a structured relational database to centralize hostel-related information and maintain relationships between different entities.

## 🎯 Objectives

* Manage student information
* Manage hostels, floors, rooms, and beds
* Track student room/bed allocations
* Record hostel payments
* Manage student complaints
* Manage hostel staff
* Track maintenance requests
* Maintain relationships between different hostel entities
* Reduce data redundancy through database normalization

## 🗂️ Main Entities

The database contains the following major entities:

* **Hostel**
* **Floor**
* **Room**
* **Bed**
* **Student**
* **Allocation**
* **Payment**
* **Complaint**
* **Staff**
* **Maintenance Request**
* **Staff Maintenance**

## 🔗 Database Relationships

The system models relationships such as:

```text
Hostel
   │
   └── Floor
         │
         └── Room
               │
               └── Bed
                     │
                     └── Allocation
                           │
                           └── Student

Student
   ├── Payment
   └── Complaint

Staff
   └── Staff Maintenance
             │
             └── Maintenance Request
```

## 🧠 DBMS Concepts Used

This project demonstrates several core DBMS concepts:

* Relational database design
* Entity-Relationship (ER) modeling
* Primary Keys
* Foreign Keys
* Candidate Keys
* Composite Keys
* Referential Integrity
* Functional Dependencies
* Normalization
* BCNF
* 5NF
* SQL queries
* Data manipulation
* Data integrity constraints

## 🏗️ Database Design

The database was designed with normalization in mind to minimize redundancy and improve data consistency.

The schema separates hostel-related information into multiple related tables rather than storing all information in a single table.

### Example relationship

A hostel can contain multiple floors, each floor can contain multiple rooms, and each room can contain multiple beds.

```text
Hostel → Floor → Room → Bed
```

Students are then connected to beds through the **Allocation** entity.

## 💻 Technologies

* **SQL**
* **Relational Database Management System (RDBMS)**
* **ER Diagram**
* **Database Normalization**
* **DBMS Concepts**

## 📁 Repository Structure

```text
hostel-management-database/
│
├── database/
│   ├── schema.sql
│   ├── tables.sql
│   ├── relationships.sql
│   └── sample_data.sql
│
├── er-diagram/
│   └── hostel-management-erd.png
│
├── documentation/
│   └── DBMS_Project_Report.pdf
│
└── screenshots/
    └── database.png
```

## 🚀 Key Features

### Student Management

Stores and manages student information and hostel-related records.

### Room & Bed Management

Maintains information about hostels, floors, rooms, and individual beds.

### Allocation Management

Tracks which student is assigned to which bed and manages allocation records.

### Payment Management

Records hostel-related payments and payment information.

### Complaint Management

Allows complaints to be recorded and associated with students.

### Maintenance Management

Tracks maintenance requests and the staff members responsible for handling them.

## 📊 ER Diagram

The complete Entity-Relationship Diagram is available in:

`er-diagram/hostel-management-erd.png`

## 🔍 Example SQL Operations

The database supports queries such as:

```sql
-- Find students currently allocated to hostel rooms
SELECT *
FROM Student
JOIN Allocation
ON Student.student_id = Allocation.student_id;
```

Other queries can be used to analyze:

* Available beds
* Student allocations
* Payment records
* Pending complaints
* Maintenance requests
* Staff assignments
* Room occupancy

## 📚 Learning Outcomes

Through this project, I developed practical experience with:

* Relational database design
* ER modeling
* SQL
* Database normalization
* Entity relationships
* Constraints and referential integrity
* Translating real-world requirements into a database schema

  Author

Md. Riyad Ahmed Hridoy

BSc in Data Science and Analytics
East West University, Bangladesh

