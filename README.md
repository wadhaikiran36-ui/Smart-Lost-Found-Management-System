# Smart Lost & Found Management System

## 1. Project Overview

The Smart Lost & Found Management System is a Java-based application developed as a college project for the Programming in Java course.

The project provides a centralized platform for managing lost and found items in educational institutions and organizations.

Users can report lost items, report found items, search for items, view possible matches, and submit claims. The system also includes a smart weighted matching engine that compares item details and generates match scores.

The backend is implemented using Java Servlets, JDBC, MySQL, and Apache Tomcat. The project also demonstrates important Object-Oriented Programming concepts such as abstraction, inheritance, polymorphism, encapsulation, collections, exception handling, and database connectivity.

Live Project:

YOUR_DEPLOYED_PROJECT_URL

---

## 2. Features

- Centralized Lost & Found Dashboard
- User registration
- User login
- Student management
- Administrator management
- Lost item reporting
- Found item reporting
- Item details and status management
- Search and filtering
- Smart Lost–Found Matching Engine
- Category-based matching
- Item name similarity
- Location similarity
- Color matching
- Brand matching
- Date proximity matching
- Description keyword matching
- Match score calculation
- High, Medium, Low, and Unlikely match classification
- Match result visualization
- Claim submission
- Claim management
- Administrator verification
- Item status tracking
- Responsive user interface
- Modern interface
- Java-based backend
- MySQL database integration

---

## 3. Technologies / Tools Used

### Java

Used for implementing the backend functionality, object-oriented programming concepts, servlets, services, data access objects, collections, validation, and the smart matching engine.

### Java Servlets

Used to handle HTTP requests and provide backend functionality for login, registration, lost items, found items, searches, matches, claims, and administration.

### JDBC

Used to connect the Java application with the MySQL database and perform database operations using PreparedStatement.

### MySQL

Used for storing users, items, matches, and claims.

### HTML

Used for creating the structure of the web interface.

### CSS

Used for styling, responsive layouts, and the overall visual appearance of the application.

### JavaScript / TypeScript

Used for frontend interaction, navigation, dynamic content, and application functionality.

### React

Used for developing the frontend user interface and reusable components.

### Vite

Used as the frontend development and build tool.

### Google AI Studio

Used during the development of the web application.

### GitHub

Used for source-code management, version control, and project submission.

### Apache Tomcat

Used as the web server for deploying and running the Java Servlet backend.

### Maven

Used for managing Java project dependencies and building the backend application.

---

## 4. Steps to Install and Run the Project

### Step 1: Clone the Repository

Clone the GitHub repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL

Replace YOUR_GITHUB_REPOSITORY_URL with the actual GitHub repository URL.

Step 2: Open the Project

Open the downloaded project folder using a suitable code editor such as:

VS Code
IntelliJ IDEA
Eclipse
Step 3: Configure the Database

Open MySQL and create the required database.

Run the SQL schema provided in:

backend-java/database/schema.sql

The database used by the project is:

lost_found_system

Configure the database connection details in the Java backend according to your local MySQL setup.

Step 4: Build the Java Backend

Navigate to the Java backend directory:

cd backend-java

Build the project using Maven:

mvn clean package

After successful compilation, the WAR file will be generated inside:

backend-java/target/
Step 5: Deploy the Java Backend

Deploy the generated WAR file to an Apache Tomcat server.

The backend can then be accessed through the Tomcat server.

Example:

http://localhost:8080/lost-found-system/
Step 6: Install Frontend Dependencies

Navigate to the project root directory and install the required packages:

npm install
Step 7: Configure Environment Variables

Create or configure the .env.local file according to the project requirements.

Example:

GEMINI_API_KEY=YOUR_API_KEY

Replace YOUR_API_KEY with the required API key if the corresponding functionality is being used.

Step 8: Run the Web Application

Start the frontend development server:

npm run dev

The application will be available at the local URL displayed by Vite, normally similar to:

http://localhost:5173/
5. Instructions for Testing
Web Application Testing

Open the application and test the following modules:

Landing Page
User Registration
User Login
Student Dashboard
Admin Dashboard
Report Lost Item
Report Found Item
Search Items
Match Results
Claims
Item Status
Administrative Management

Check the navigation, buttons, forms, search functionality, item reporting, match results, and claim-related components to verify that they work correctly.

Smart Matching Testing

Test the matching functionality using lost and found items with similar details.

The matching engine evaluates:

Category
Item Name
Location
Color
Brand
Date
Description

The system calculates a weighted matching score and classifies the result as:

80–100  → High Match
60–79   → Medium Match
40–59   → Low Match
Below 40 → Unlikely Match

Verify that similar lost and found items receive higher matching scores than unrelated items.

Java Backend Testing

Navigate to the backend directory:

cd backend-java

Compile and build the Java project:

mvn clean package

The Java implementation can be tested through the application and the backend verification functionality.

Verify the implemented Java concepts, including:

Object creation
Abstraction
Inheritance
Polymorphism
Encapsulation
ArrayList operations
HashSet operations
JDBC database connectivity
PreparedStatement usage
Input validation
Password hashing
Item processing
Smart matching
Claim processing
Exception and error handling
6. Project Structure
Smart-Lost-and-Found-Management-System/
│
├── backend-java/
│   ├── src/
│   │   └── main/
│   │       └── java/
│   │           └── com/
│   │               └── lostfound/
│   │                   ├── model/
│   │                   ├── dao/
│   │                   ├── service/
│   │                   ├── controller/
│   │                   └── util/
│   │
│   ├── database/
│   │   └── schema.sql
│   │
│   ├── pom.xml
│   └── README.md
│
├── src/
│   ├── components/
│   ├── services/
│   ├── data/
│   ├── App.tsx
│   ├── main.tsx
│   └── types.ts
│
├── package.json
├── vite.config.ts
├── index.html
└── README.md
7. Java Modules

The Java backend is organized into different packages.

Model

Contains classes representing the main entities:

User
Student
Admin
Item
LostItem
FoundItem
Match
Claim
DAO

Handles database operations:

UserDAO
ItemDAO
MatchDAO
ClaimDAO
Service

Contains application and business logic:

LoginService
UserService
ItemService
MatchingService
ClaimService
Controller

Contains Java Servlets responsible for handling requests:

LoginServlet
RegisterServlet
LostItemServlet
FoundItemServlet
SearchServlet
MatchServlet
ClaimServlet
AdminServlet
Utility

Contains supporting classes:

DatabaseConnection
PasswordUtil
ValidationUtil
8. Smart Matching Algorithm

The project uses a weighted matching system to identify possible relationships between lost and found items.

The matching score is calculated using seven criteria:

Matching Criterion	Weight
Category Match	20%
Item Name Similarity	20%
Location Similarity	20%
Color Match	10%
Brand Match	10%
Date Proximity	10%
Description Similarity	10%

The final score helps users identify the most likely matching found item for a lost item.

9. Java Concepts Demonstrated

The project demonstrates several important Java programming concepts:

Abstraction

Abstract classes such as User and Item provide common structures for related classes.

Inheritance

Classes such as Student and Admin inherit from User.

LostItem and FoundItem inherit from Item.

Polymorphism

Methods are overridden in child classes to provide specialized behavior.

Encapsulation

Data members are protected using appropriate access modifiers and accessed through getters and setters.

Collections

Java collections such as ArrayList and HashSet are used for managing groups of objects and unique values.

JDBC

JDBC is used to connect Java with MySQL and perform database operations.

Exception Handling

Errors and invalid operations are handled to improve application reliability.
