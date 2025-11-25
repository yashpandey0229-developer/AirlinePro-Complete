✈️ AirlinePro: A Full-Stack Airline Reservation System
AirlinePro is a comprehensive, web-based airline booking application built using a modern full-stack architecture. It allows users to search for flights, book tickets, and manage their reservations, while providing administrators with tools to manage flight schedules and customer data securely.

🚀 Features
👤 User (Customer) Features
Secure Registration & Login: Users can create an account and log in securely using JWT (JSON Web Token) authentication.

Search Flights: Search for available flights by origin and destination.

Book Tickets: Real-time seat booking that updates flight availability instantly.

My Bookings: View a personal dashboard of all confirmed bookings with current status.

Cancel Booking: Ability to cancel reservations, which automatically restores seat availability.

🛠️ Admin Features
Flight Management: Add new flights, edit existing flight details, and delete flights.

Customer Management: View a list of all registered customers, add new customers manually, and manage their profiles.

Role-Based Access: Admin controls (Add/Edit/Delete) are hidden and protected from regular users.

🏗️ Tech Stack
Backend
Language: Java 21

Framework: Spring Boot 3.3.0

Security: Spring Security, JWT (JSON Web Tokens), BCrypt

Database: MySQL (Spring Data JPA)

Build Tool: Maven

Frontend
Library: React.js (Vite)

Routing: React Router v6
📂 Project Structure
The project follows a Monorepo structure:

Plaintext

AirlinePro/
├── Backend/           # Java Spring Boot Application
│   ├── src/
│   ├── pom.xml
│   └── ...
└── Frontend/          # React Vite Application
    ├── src/
    ├── package.json
    └── ...
State Management: React Context API (for Authentication state)

Styling: CSS (Glassmorphism design)
