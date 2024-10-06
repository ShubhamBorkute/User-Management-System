# User-Management-System
 This project is a User Management System that allows users to perform CRUD (Create, Read, Update, Delete).
Technical Specification Document
1. Project Overview
This project is a User Management System that allows users to perform CRUD
(Create, Read, Update, Delete) operations for managing user details. The system
will collect the following user details:
• First Name
• Last Name
• Phone Number
• Email ID
• Address
 The application will feature:
• A user-friendly interface for managing users.
• Server-side validation to ensure data integrity.
• Persistent storage using a relational database (MySQL).
2. Objectives
 The primary objectives of the application are:
1. Collect User Data: Allow users to input basic details like first name, last
name, phone number, email ID, and address.
2. Data Management: Enable CRUD operations to manage users effectively.
3. Data Validation: Implement data validation to ensure accurate and
complete user data.
4. Database Persistence: Store user details in a database with efficient CRUD
operations.
3. Technology Stack
 The following technologies will be used in the application:
 3.1 Backend
1. Spring Boot (Java): For building the application with RESTful APIs.
2. Spring Data JPA: For database interaction using Object Relational Mapping
(ORM).
3. Spring Validation: For validating input data.
 3.2 Frontend
• Thymeleaf: Template engine for rendering HTML pages with dynamic
content.
• HTML5/CSS3: For building the structure and styling of the web pages.
• JavaScript: For client-side interaction, if necessary (optional).
 3.3 Database
1. MySQL: A relational database to persist user details.
4. System Design
4.1 Architecture
 The application will follow the Model-View-Controller (MVC) architecture:
1. Model: Represents the user entity and interacts with the database.
2. View: Thymeleaf templates render user interfaces for CRUD operations.
3. Controller: Manages the application logic, handling requests and
responses.
4.2 Components
1. UserEntity: A Java class that represents a user in the system with fields such
as first name, last name, phone number, email ID, and address.
2. UserRepository: A Spring Data JPA repository that manages CRUD
operations for users.
3. UserController: A Spring MVC controller that handles HTTP requests and
routes them to the appropriate service methods.
4. Service Layer: (Optional) A business service layer to handle business logic.
Can be included if you plan to scale up the project in the future.
5. Database Design
 The database consists of a single table User for storing user details.
 5.1 User Table
Field Type Constraints
id Integer Primary Key, Auto-Increment
First Name String Not Null, Min 2, Max 30 chars
Last Name String Not Null, Min 2, Max 30 chars
Phone Number String Not Null, Unique, 10 digits
Email String Not Null, Unique, Valid Email
Address String Not Null, Min 5, Max 100 chars
5.2 Constraints
• Phone Number: Must be a 10-digit valid number.
• Email ID: Must be a valid email address.
• First Name/Last Name: Cannot be empty and should follow specific length
constraints.
6. Functional Requirements
1. Create User:
• A form will be provided to enter user details.
• Fields will include First Name, Last Name, Phone Number, Email ID,
and Address.
• Validation will ensure data accuracy before submission.
2. Read/View Users:
• A list of all users will be displayed.
• Users will be listed with options to view their details, update, or
delete.
3. Update User:
• A user can update their details.
• The system will validate the updated information.
4. Delete User:
• A user can be deleted from the system.
• A confirmation step will be provided before deletion.
7. Non-Functional Requirements
1. Data Validation: Ensure data is validated both on the client-side (via
HTML5 attributes) and server-side (via Spring Validation).
2. Security: Use basic security features to prevent SQL injection and
other common attacks. (Optional: Use Spring Security for login
functionality.)
3. Performance: Ensure efficient database operations using Spring Data
JPA.
4. Scalability: Design the system to support additional features like
user authentication and more advanced user management in the
future.
8. Validation Logic
 8.1 Validation Rules
• First Name: Must be between 2 and 30 characters, cannot be empty.
• Last Name: Must be between 2 and 30 characters, cannot be empty.
• Phone Number: Must be a valid 10-digit number.
• Email ID: Must be a valid email format (e.g., user@gmail.com).
• Address: Must be between 5 and 100 characters, cannot be empty.
 8.2 Validation Annotations
Here are the validation annotations applied in the User entity:

9. UI Design
9.1 Add/Edit User Form
• A form with fields: First Name, Last Name, Phone Number, Email,
Address.
• Submit button to create/update the user.
• Validation messages will be displayed under each field if input is invalid.
9.2 User List
• Displays a table of users with columns for each field.
• Buttons for Edit and Delete will be available next to each user.
9.3 Validation Feedback
• If a user submits invalid data, the form will reload with validation error
messages under the affected fields.
10. Testing Strategy
10.1 Unit Tests
• Test validation rules using Spring Boot's unit testing capabilities.
10.2 Integration Tests
• Test end-to-end functionality: form submissions, database persistence,
and CRUD operations.
10.3 User Acceptance Testing
• Ensure the application meets the functional requirements and is userfriendly.
11. Error Handling
• Display user-friendly error messages for invalid inputs.
• Catch common exceptions (e.g., database errors) and show a custom
error page.
12. Deployment
The application can be deployed on a local or remote server.
• Tomcat (embedded with Spring Boot)
Conclusion
 This document outlines the detailed technical specifications for the
User Management System. The project follows best practices for building a
maintainable, scalable, and user-friendly web application using Spring Boot,
Spring Data JPA, Lombok and Thymeleaf.
