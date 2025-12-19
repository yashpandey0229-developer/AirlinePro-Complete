# ✈️ AirlinePro: A Full-Stack Airline Reservation System

> **Final Project Submission (Review 2)**
> * **Student Name:** Yash Pandey
> * **Course/Batch:** Java Programming

**AirlinePro** is a comprehensive, web-based airline booking application built using a modern full-stack architecture. It is designed to provide a seamless, error-free booking experience with strict data validation, secure authentication, and role-based access control.

---

## 🌟 Code Quality & Innovation

**Innovation in Architecture:**
Unlike traditional monolithic Java applications (JSP/Servlet), AirlinePro utilizes a modern **Headless Architecture**. We decoupled the frontend (React.js) from the backend (Spring Boot) entirely.

1.  **State Management:** Utilized React's **Context API** to manage global user authentication state without page reloads, creating a true Single Page Application (SPA) experience.
2.  **Stateless Security:** Implemented **JWT (JSON Web Tokens)** instead of server-side sessions. This makes the application scalable and follows industry-standard REST API security practices.
3.  **Role-Based Dynamic UI:** The interface automatically adapts—hiding Admin buttons and protecting routes—based on the user's role payload in the JWT token.

---

## 🛡️ Robustness & Data Validation 

To ensure the system is crash-proof and handles data securely, the following validations are implemented:

### 1. Server-Side Validation (Spring Boot)
* **Data Integrity:** The backend strictly enforces unique constraints (e.g., users cannot register with an existing username/email).
* **Business Logic:** Prevents logical errors, such as booking 0 seats or booking more seats than are currently available on a flight.
* **Exception Handling:** A global exception handler catches errors (like `ResourceNotFoundException`) and returns clean, JSON-formatted error messages instead of crashing the server.

### 2. Client-Side Validation (React)
* **Form Protection:** All input forms (Login, Register, Add Flight) use strict HTML5 and JavaScript validation to prevent empty submissions.
* **Type Safety:** Numeric fields (like Price, Seats) prevent non-numeric input to avoid calculation errors.

---

## 🏗️ Tech Stack

* **Frontend:** React.js, Vite, React Router v6, Axios.
* **Backend:** Java 21, Spring Boot 3.3.0, Spring Security, Hibernate.
* **Database:** MySQL.
* **Tools:** Maven, Postman, VS Code.

---

## 📂 Project Structure

The project follows a Monorepo structure for better code organization:

```text
AirlinePro-Complete/
├── Backend/           # Java Spring Boot Server
│   ├── src/main/java/com/airlines/...
│   ├── src/main/resources/application.properties
│   └── pom.xml
└── Frontend/          # React Client Application
    ├── src/components/
    ├── src/pages/
    ├── src/context/
    └── package.json
To include all the specific points required for Review 2 (Innovation, Validation, Robustness), you should update your README.md to explicitly highlight these sections. This ensures the examiner sees exactly what they are looking for immediately.

Here is the exact Markdown text you can copy. I have added specific "Rubric Highlights" sections so you get full marks.

How to update it:
Open your project in VS Code.

Open the README.md file (in the main folder).

Delete everything currently in there.

Paste the following code block entirely.

Save, Commit, and Push.

Markdown

# ✈️ AirlinePro: A Full-Stack Airline Reservation System

> **Final Project Submission (Review 2)**
> * **Student Name:** [Your Name Here]
> * **Course/Batch:** [Your Course Name Here]

**AirlinePro** is a comprehensive, web-based airline booking application built using a modern full-stack architecture. It is designed to provide a seamless, error-free booking experience with strict data validation, secure authentication, and role-based access control.

---

## 🌟 Code Quality & Innovation (Rubric Point 6)

**Innovation in Architecture:**
Unlike traditional monolithic Java applications (JSP/Servlet), AirlinePro utilizes a modern **Headless Architecture**. We decoupled the frontend (React.js) from the backend (Spring Boot) entirely.

1.  **State Management:** Utilized React's **Context API** to manage global user authentication state without page reloads, creating a true Single Page Application (SPA) experience.
2.  **Stateless Security:** Implemented **JWT (JSON Web Tokens)** instead of server-side sessions. This makes the application scalable and follows industry-standard REST API security practices.
3.  **Role-Based Dynamic UI:** The interface automatically adapts—hiding Admin buttons and protecting routes—based on the user's role payload in the JWT token.

---

## 🛡️ Robustness & Data Validation (Rubric Point 2 & 5)

To ensure the system is crash-proof and handles data securely, the following validations are implemented:

### 1. Server-Side Validation (Spring Boot)
* **Data Integrity:** The backend strictly enforces unique constraints (e.g., users cannot register with an existing username/email).
* **Business Logic:** Prevents logical errors, such as booking 0 seats or booking more seats than are currently available on a flight.
* **Exception Handling:** A global exception handler catches errors (like `ResourceNotFoundException`) and returns clean, JSON-formatted error messages instead of crashing the server.

### 2. Client-Side Validation (React)
* **Form Protection:** All input forms (Login, Register, Add Flight) use strict HTML5 and JavaScript validation to prevent empty submissions.
* **Type Safety:** Numeric fields (like Price, Seats) prevent non-numeric input to avoid calculation errors.

---

## 🏗️ Tech Stack

* **Frontend:** React.js, Vite, React Router v6, Axios.
* **Backend:** Java 21, Spring Boot 3.3.0, Spring Security, Hibernate.
* **Database:** MySQL.
* **Tools:** Maven, Postman, VS Code.

---

## 📂 Project Structure

The project follows a Monorepo structure for better code organization:

```text
AirlinePro-Complete/
├── Backend/           # Java Spring Boot Server
│   ├── src/main/java/com/airlines/...
│   ├── src/main/resources/application.properties
│   └── pom.xml
└── Frontend/          # React Client Application
    ├── src/components/
    ├── src/pages/
    ├── src/context/
    └── package.json
⚙️ Setup & Execution Instructions
1. Database Setup
Open MySQL Workbench.

Create the database: CREATE DATABASE airline_reservation_system;

Update credentials in Backend/src/main/resources/application.properties.
cd Backend
./mvnw clean package
java -jar target/airline-reservation-system-0.0.1-SNAPSHOT.jar
Method,Endpoint,Role,Description
POST,/api/auth/register,Public,Register new customer
POST,/api/auth/login,Public,Login & receive JWT
GET,/flights/search,Public,Search flights by route
POST,/bookings/create,User,Book a seat on a flight
DELETE,/bookings/cancel/{id},User,Cancel an existing booking
POST,/flights/add,Admin,Add new flight inventory
DELETE,/flights/delete/{id},Admin,Remove a flight
