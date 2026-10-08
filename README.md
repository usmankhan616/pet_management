# 🐾 Pet Care Management System

## 📌 Project Overview

**Pet Care Management System** is a full-stack web application developed to help pet owners manage their pets and their pet-care-related information through a centralized platform.

The application provides a user-friendly interface where users can manage pet information and interact with the backend through REST APIs.

The project was developed as part of an **Infosys Springboard project/milestone**.

---

## 🎯 Objective

The main objective of this project was to build a full-stack application using **React and Spring Boot** while implementing:

- User authentication and security
- Pet management
- CRUD operations
- RESTful APIs
- Database persistence
- Frontend-backend integration
- Secure access to application resources

---

# 🏗️ Application Architecture

The application follows a typical **3-tier / client-server architecture**.

```text
                    ┌─────────────────────┐
                    │     React Frontend  │
                    │    Pet Care UI      │
                    └──────────┬──────────┘
                               │
                         HTTP / REST API
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Spring Boot      │
                    │     Backend        │
                    ├─────────────────────┤
                    │ Controllers        │
                    │ Services           │
                    │ Repositories       │
                    │ Security           │
                    └──────────┬──────────┘
                               │
                         JPA / Hibernate
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MySQL        │
                    │      Database      │
                    └─────────────────────┘
```

---

# 🔄 Application Flow

The basic flow of the application is:

```text
User
 │
 ▼
React Frontend
 │
 │ HTTP Request
 ▼
Spring Boot REST Controller
 │
 ▼
Service Layer
 │
 ▼
Spring Data JPA Repository
 │
 ▼
MySQL Database
 │
 │ Data
 ▼
Repository
 │
 ▼
Service
 │
 ▼
REST Controller
 │
 │ HTTP Response
 ▼
React Frontend
 │
 ▼
User
```

### Example

When a user wants to add a pet:

```text
User enters pet details
        ↓
React sends POST request
        ↓
Spring Boot Controller receives request
        ↓
Service processes the request
        ↓
JPA Repository saves the pet
        ↓
MySQL stores the data
        ↓
Response is returned to React
        ↓
Pet information is displayed
```

---

# 🛠️ Technologies Used

## Backend

| Technology | Purpose |
|---|---|
| **Java** | Main programming language |
| **Spring Boot** | Backend application framework |
| **Spring Web** | Building REST APIs |
| **Spring Data JPA** | Database operations |
| **Hibernate** | ORM / object-relational mapping |
| **Spring Security** | Authentication and authorization |
| **Lombok** | Reducing boilerplate Java code |
| **Maven** | Dependency and build management |

## Frontend

| Technology | Purpose |
|---|---|
| **React** | Building the user interface |
| **JavaScript / JSX** | Frontend programming |
| **HTML/CSS** | UI structure and styling |

## Database

| Technology | Purpose |
|---|---|
| **MySQL** | Storing application data |
| **JPA/Hibernate** | Communicating between Java objects and database tables |

---

# ⚙️ Backend Structure

The Spring Boot backend follows a layered architecture.

```text
src/
 └── main/
      └── java/
           └── ...
                ├── Controller
                ├── Service
                ├── Repository
                ├── Entity
                └── Security
```

### Controller Layer

Responsible for handling HTTP requests and exposing REST endpoints.

```text
Client
  ↓
Controller
```

For example:

```text
GET    → Retrieve data
POST   → Create data
PUT    → Update data
DELETE → Delete data
```

---

### Service Layer

Contains the application's business logic.

```text
Controller
     ↓
 Service
     ↓
Repository
```

The service layer keeps business logic separate from the controller and database access code.

---

### Repository Layer

Uses **Spring Data JPA** to communicate with the database.

```text
Service
   ↓
Repository
   ↓
MySQL
```

This reduces the amount of SQL/database boilerplate code required.

---

### Entity Layer

Java classes represent the application's database entities.

Hibernate/JPA maps these Java objects to relational database tables.

```text
Java Entity
     ↕
Database Table
```

---

# 🔐 Security

The project uses **Spring Security** to protect application resources.

Security is responsible for controlling access to backend resources and handling authentication/authorization requirements.

The general flow is:

```text
User
 ↓
Authentication
 ↓
Spring Security
 ↓
Authorization
 ↓
Protected REST API
```

This adds an additional security layer between the frontend and backend.

---

# 🐶 Pet Management

The main purpose of the application is managing pet-related information.

Typical operations include:

```text
Create Pet
    ↓
Read Pet
    ↓
Update Pet
    ↓
Delete Pet
```

These operations are implemented using REST APIs and persisted in MySQL.

---

# 🔗 Frontend ↔ Backend Communication

The React frontend communicates with the Spring Boot backend through **REST APIs**.

```text
React
  │
  │ HTTP Request
  ▼
Spring Boot REST API
  │
  ▼
Business Logic
  │
  ▼
MySQL
```

The backend returns the requested data to the React application, which then updates the user interface.

---

# 📊 Database Flow

The application uses **MySQL** for persistent data storage.

```text
React
 ↓
REST API
 ↓
Spring Boot
 ↓
Spring Data JPA
 ↓
Hibernate
 ↓
MySQL
```

Hibernate handles the mapping between Java entities and database tables.

---

# ✨ Key Features

- User-friendly pet management interface
- Pet information management
- CRUD operations
- RESTful backend APIs
- MySQL database integration
- Spring Data JPA integration
- Hibernate ORM
- Spring Security integration
- React frontend
- Layered Spring Boot architecture
- Frontend and backend integration

---

# 🧑‍💻 My Technical Contribution

Through this project, I worked with and gained practical experience in:

### Java & Spring Boot

- Developing REST APIs
- Creating controllers and services
- Implementing repository-based database access
- Working with Spring Boot configuration
- Using Spring Data JPA
- Working with Hibernate

### Database

- Designing and working with MySQL tables
- Persisting application data
- Using JPA entities
- Performing CRUD operations

### Security

- Working with Spring Security
- Understanding authentication and authorization
- Securing backend resources

### Frontend

- Developing UI using React
- Connecting React with Spring Boot APIs
- Handling data received from REST APIs

### Development Tools

- Maven
- Git
- GitHub
- VS Code / IDE
- MySQL

---

# 🧠 What I Learned

This project helped me understand how a real-world full-stack application is structured.

The major concepts I learned were:

1. How React communicates with a Spring Boot backend.
2. How REST APIs are created using Spring Boot.
3. How controllers, services, and repositories work together.
4. How Java objects are mapped to database tables using JPA/Hibernate.
5. How MySQL is integrated with a Spring Boot application.
6. How Spring Security is used to protect backend resources.
7. How frontend and backend applications work together as a complete system.
8. How to manage and maintain a project using Git and GitHub.

---

# 🚀 Overall Technology Flow

```text
                 PET CARE MANAGEMENT SYSTEM

                         👤 User
                           │
                           ▼
                    React Frontend
                           │
                           │ REST / HTTP
                           ▼
                  Spring Boot Backend
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Controller      Service       Security
             │             │
             └──────┬──────┘
                    ▼
             Spring Data JPA
                    │
                    ▼
               Hibernate ORM
                    │
                    ▼
                  MySQL
                    │
                    ▼
             Persistent Data
```

---

# 📁 Project Structure

```text
pet_management/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── Spring Boot backend
│       │
│       └── resources/
│           └── application.properties
│
├── pet-care-frontend/
│   └── React frontend
│
├── scripts/
│
├── pom.xml
│
├── infosys_milestone.txt
│
└── README / Project Documentation
```

---

# 📌 Project Summary

**Pet Care Management System** is a full-stack web application built using **React, Java Spring Boot, Spring Data JPA, Hibernate, Spring Security, and MySQL**.

The project demonstrates how a modern web application can be structured using a **React frontend, RESTful Spring Boot backend, layered architecture, secure APIs, and a relational database**.

The project provided practical experience in **full-stack development, REST API development, database integration, security, and frontend-backend communication**.

---

## 🧾 One-Line Interview Explanation

> **"I worked on a full-stack Pet Care Management System using React for the frontend and Java Spring Boot for the backend, where I implemented REST APIs, CRUD operations, Spring Data JPA/Hibernate for MySQL database integration, and Spring Security for securing application resources."**

---

## 🎤 Short Interview Version

If an interviewer asks **"Tell me about your project"**, you can say:

> "My project was a Pet Care Management System developed as part of the Infosys Springboard program. It is a full-stack application where React is used for the frontend and Java Spring Boot is used for the backend. The backend follows a layered architecture with controllers, services, repositories and entities. I used Spring Data JPA and Hibernate to interact with MySQL and Spring Security for authentication and authorization. The frontend communicates with the backend through REST APIs, allowing users to perform operations such as managing pet information. Through this project, I gained practical experience in Spring Boot, REST APIs, JPA, Hibernate, MySQL, Spring Security and React."
