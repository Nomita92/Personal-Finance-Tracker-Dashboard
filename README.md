# Personal Finance Tracker Dashboard

## Product Requirements Document (PRD)

**Version:** 1.0  
**Author:** Nomita Patwal  
**Project Type:** Personal Portfolio Project  
**Tech Stack:** Java, Spring Boot, HTML, CSS, Thymeleaf, MySQL  

---

# 1. Product Overview

The **Personal Finance Tracker Dashboard** is a web-based application that allows users to track and manage their daily expenses through an interactive dashboard interface.

The system provides a centralized dashboard where users can:

- Add new expenses
- View recent transactions
- Monitor total spending
- Analyze spending by category

Unlike simple expense trackers, this project emphasizes a **modern dashboard-style UI** using a **green financial theme**, making the interface intuitive and visually organized.

The project demonstrates **full-stack development using Spring Boot with a MySQL database and server-rendered HTML pages**.

---

# 2. Product Goals

## Primary Goals

- Provide a simple interface to log daily expenses
- Display financial information using a dashboard layout
- Allow users to view and manage transactions
- Show expense summaries and spending insights

## Secondary Goals

- Demonstrate Spring Boot MVC architecture
- Implement CRUD operations with database persistence
- Create a portfolio-ready backend project

---

# 3. Target Users

### Students
Students who want to track daily expenses such as food, transportation, and subscriptions.

### Young Professionals
Individuals who want a quick overview of their spending habits.

### Budget-conscious individuals
Users who want to maintain awareness of their spending patterns.

---

# 4. Core Features

## Dashboard Overview

The dashboard is the central page of the application and provides a summary of financial activity.

The dashboard displays:

- Total expenses
- Total number of transactions
- Highest spending category
- Recent transactions list

---

## Add Expense

Users can add new expense entries using a simple form.

### Fields

| Field | Description |
|------|-------------|
| Title | Name of the expense |
| Amount | Amount spent |
| Category | Expense category |
| Date | Transaction date |

After submission, the expense is saved to the database and automatically appears on the dashboard.

---

## Expense Table

The dashboard includes a table displaying recent transactions.

| Column | Description |
|------|-------------|
| Title | Expense name |
| Category | Expense category |
| Amount | Expense amount |
| Date | Date of transaction |
| Action | Delete expense |

---

## Delete Expense

Users can remove an expense entry from the system.

Once deleted, the dashboard automatically updates.

---

## Expense Summary Cards

The dashboard shows key financial insights through summary cards:

- Total Expenses
- Total Transactions
- Top Spending Category

These cards provide a quick overview of financial activity.

---

# 5. Functional Requirements

| ID | Requirement |
|----|-------------|
| FR-1 | User should be able to add a new expense |
| FR-2 | User should be able to view all expenses |
| FR-3 | User should be able to delete expenses |
| FR-4 | System should calculate total expense automatically |
| FR-5 | System should display recent transactions on the dashboard |

---

# 6. Non-Functional Requirements

| Requirement | Description |
|-------------|-------------|
| Performance | Dashboard should load quickly |
| Usability | Interface should be simple and intuitive |
| Maintainability | Code should follow MVC architecture |
| Scalability | System should allow future feature additions |

---

# 7. UI / UX Design

The application uses a **modern fintech-inspired dashboard interface** with a **green color theme** representing financial growth and money management.

## Color Theme

| UI Element | Color |
|------------|-------|
| Primary Green | #2ecc71 |
| Dark Green | #27ae60 |
| Light Background | #ecfdf5 |
| Card Background | #ffffff |
| Text | #1f2937 |

---

# 8. Database Design (MySQL)

The system uses **MySQL as the primary database** to store expense records.

MySQL is chosen because it is reliable, scalable, and integrates well with Spring Boot.

## Database Name

expense_tracker_db

## Expense Table Schema

| Column | Data Type | Description |
|------|-----------|-------------|
| id | BIGINT | Primary key |
| title | VARCHAR(255) | Expense title |
| amount | DECIMAL(10,2) | Amount spent |
| category | VARCHAR(100) | Expense category |
| date | DATE | Transaction date |

## SQL Table Creation

```sql
CREATE DATABASE expense_tracker_db;

USE expense_tracker_db;

CREATE TABLE expenses (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    amount DECIMAL(10,2) NOT NULL,
    category VARCHAR(100),
    date DATE
);
```

---

# 9. System Architecture

The application follows the **Model–View–Controller (MVC)** architecture.

```
Browser (Client)
       ↓
Spring Boot Controller
       ↓
Service Layer (Business Logic)
       ↓
Repository Layer (Spring Data JPA)
       ↓
MySQL Database
```

---

# 10. Technology Stack

## Backend
- Java
- Spring Boot
- Spring MVC
- Spring Data JPA

## Frontend
- HTML
- CSS
- Thymeleaf

## Database
- MySQL

---

# 11. Project Structure

```
expense-tracker-dashboard
│
├── controller
│     DashboardController.java
│     ExpenseController.java
│
├── service
│     ExpenseService.java
│
├── repository
│     ExpenseRepository.java
│
├── model
│     Expense.java
│
├── templates
│     dashboard.html
│     add-expense.html
│
└── static
      css
        styles.css
```

---

# 12. Data Flow

```
User submits expense form
        ↓
Controller receives request
        ↓
Service processes logic
        ↓
Repository saves data
        ↓
Hibernate generates SQL
        ↓
MySQL stores expense
        ↓
Dashboard updates
```

---

# 13. Future Enhancements

Possible improvements in future versions:

- User authentication system
- Monthly expense analytics
- Charts and graphs using Chart.js
- Budget limits and alerts
- Expense filtering by date
- Export expenses to CSV

---

# 14. Success Criteria

The project will be considered successful if:

- Users can add expenses successfully
- Expenses are stored in MySQL database
- Dashboard updates dynamically
- Financial summaries are calculated correctly
- The UI provides a clear dashboard overview of financial activity

---

# 15. Conclusion

The **Personal Finance Tracker Dashboard** provides a clean and efficient solution for tracking daily expenses.

This project demonstrates practical implementation of:

- Spring Boot backend development  
- MySQL database integration  
- Modern dashboard UI design  

It serves as a **portfolio-ready full-stack project built using Java and Spring Boot**.
