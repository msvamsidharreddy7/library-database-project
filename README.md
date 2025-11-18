# 📚 Library Database Management System  
### CS 504 – Final Project  
**Developer:** Sai Vamsidhar Reddy Meruva.  
**Tech:** SQL (MySQL / PostgreSQL compatible)

---

## 📘 Project Overview
This project implements a fully relational **Library Database Management System** for a university/public library environment.  
The goal was to design a scalable data model that captures:

- Books and their metadata  
- Authors and publisher details  
- Library members  
- Book loans, returns, and due-date tracking  
- Fine calculation and overdue management  
- Staff operations and library transactions  

This project demonstrates strong understanding of **database design principles**, **normalization**, and **SQL DDL/DML**.

---

## 🎯 Key Features

### **1️⃣ Normalized Relational Schema**
The database is designed using **3NF** principles:

- Avoid redundancy  
- Maintain atomic attributes  
- Support efficient joins  
- Preserve referential integrity  

### **2️⃣ Core Entities Included**
The schema includes well-structured tables such as:

- `Books`
- `Authors`
- `Publishers`
- `Members`
- `Borrowings / Loans`
- `Staff`
- `Categories`
- `Reservations`
- `Fines` (if applicable)
- Junction tables for Many-to-Many relationships  

This structure ensures clean, consistent data across all modules.

### **3️⃣ Referential Integrity**
The project uses:

- `PRIMARY KEY`  
- `FOREIGN KEY` constraints  
- `ON DELETE` and `ON UPDATE` actions  
- Uniqueness constraints  
- NOT NULL validations  

All relationships between entities are enforced at the database level.

### **4️⃣ Query-Ready Design**
The schema supports all typical library operations:

- Search books by title, author, category  
- Track issued vs. available books  
- Manage overdue items  
- Calculate fines  
- Record book returns  
- Track user borrowing history  
- Maintain staff transaction logs  

This allows seamless integration into an application layer.

---

## 🧩 ERD / Schema Design (Conceptual Overview)

**Entities:**

- **Book** *(book_id, title, ISBN, category_id, publisher_id, author_id, publication_year, copies_available)*  
- **Author** *(author_id, name, bio, country)*  
- **Publisher** *(publisher_id, name, address, contact)*  
- **Member** *(member_id, name, address, phone, email, membership_date)*  
- **Loan / Borrowing** *(loan_id, member_id, book_id, loan_date, due_date, return_date)*  
- **Fine** *(fine_id, loan_id, amount, status)*  

**Relationships:**

- A book can have **one publisher**  
- A book can have **one or many authors**  
- A member can borrow **many books**  
- Each borrowing creates **one fine record** (optional)  

---

## 🛠 SQL Features Used

✔ `CREATE TABLE` with constraints  
✔ `ALTER TABLE`  
✔ `FOREIGN KEY` with `ON DELETE CASCADE`  
✔ `CHECK` constraints  
✔ Multi-table joins  
✔ Many-to-many relationship modeling  
✔ Indexing (if used in your SQL file)  
✔ Views for easy reporting (optional)  

---



