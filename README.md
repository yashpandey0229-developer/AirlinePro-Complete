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
⚙️ Installation & Run InstructionsPrerequisitesJava JDK 17 or 21Node.js & npmMySQL Server1. Database SetupOpen MySQL Workbench.Create a new database:SQLCREATE DATABASE airline_reservation_system;
Update your database credentials in Backend/src/main/resources/application.properties:Propertiesspring.datasource.username=YOUR_MYSQL_USERNAME
spring.datasource.password=YOUR_MYSQL_PASSWORD
2. Running the Backend (Server)Open a terminal and navigate to the backend folder:Bashcd Backend
Build and run the application:Bash./mvnw clean package
java -jar target/airline-reservation-system-0.0.1-SNAPSHOT.jar
The server will start on http://localhost:8081.3. Running the Frontend (UI)Open a new terminal and navigate to the frontend folder:Bashcd Frontend/airline-ui
Install dependencies:Bash npm install
Start the development server:Bashnpm run dev
Open your browser and go to http://localhost:5173.🔑 Usage & CredentialsDefault Login CredentialsThe application includes a DatabaseSeeder that automatically creates default roles and users when you run it for the first time.Admin User:Username: adminPassword: admin(Has access to Add/Edit/Delete Flight & Customer Management)Regular User:Register a new account via the "Register" link on the homepage to test the Customer flow.📡 API EndpointsMethodEndpointDescriptionAccessPOST/api/auth/registerRegister a new userPublicPOST/api/auth/loginLogin & receive JWTPublicGET/flights/allGet all flightsPublicGET/flights/searchSearch flightsPublicPOST/flights/addAdd a new flightAdminPUT/flights/update/{id}Update flight detailsAdminDELETE/flights/delete/{id}Delete a flightAdminPOST/bookings/createBook a ticketUserDELETE/bookings/cancel/{id}Cancel a bookingUser📸 Screenshots(You can upload your screenshots to the public folder or your GitHub README directly to display them here)Home Page (Flight Search)Login PageMy Bookings Dashboard🛡️ LicenseThis project is developed for educational purposes.
