# User-Management-System
 This project is a User Management System that allows users to perform CRUD (Create, Read, Update, Delete).
Project Overview
This User Management System allows users to perform CRUD (Create, Read, Update, Delete) operations for managing user details, including:

First Name
Last Name
Phone Number
Email ID
Address
The system features:

User-friendly interface
Server-side validation
Persistent storage using MySQL
Objectives
Collect user data (first name, last name, phone number, email ID, and address)
Manage users with CRUD operations
Validate data on the server-side
Efficiently store user details in a MySQL database
Technology Stack
Backend
Spring Boot: RESTful API development
Spring Data JPA: Database interaction using ORM
Spring Validation: Input validation
Frontend
Thymeleaf: Rendering dynamic HTML content
HTML5/CSS3: Structure and styling
JavaScript: Optional client-side interactions
Database
MySQL: Relational database for user data persistence
System Design
Architecture
Follows the MVC (Model-View-Controller) pattern:

Model: Represents the user entity and interacts with the database
View: Thymeleaf templates for rendering user interfaces
Controller: Handles requests and responses
Components
UserEntity: Java class representing user fields (first name, last name, phone number, email ID, address)
UserRepository: Manages CRUD operations using Spring Data JPA
UserController: Handles HTTP requests and routes them to appropriate services
Service Layer: Optional, can be added for future scalability
Database Design
User Table
Field	Type	Constraints
id	Integer	Primary Key, Auto-Increment
first_name	String	Not Null, 2-30 characters
last_name	String	Not Null, 2-30 characters
phone	String	Not Null, Unique, 10 digits
email	String	Not Null, Unique, Valid email format
address	String	Not Null, 5-100 characters
Constraints
Phone Number: Must be 10 digits
Email: Must be a valid email format
Name Fields: Length constraints applied
Functional Requirements
Create User: Form with validation to collect user details
View Users: List of users with options to update or delete
Update User: Users can update their details with validation
Delete User: User can be deleted after confirmation
Non-Functional Requirements
Validation: Client-side (HTML5) and server-side (Spring Validation)
Security: Prevent SQL injection (optional: Spring Security)
Performance: Efficient database operations using Spring Data JPA
Scalability: Prepared for future extensions like user authentication
Validation Logic
Validation Rules
First Name: 2-30 characters, not empty
Last Name: 2-30 characters, not empty
Phone Number: Valid 10-digit number
Email ID: Valid email format
Address: 5-100 characters, not empty
Validation Annotations
Validation is applied using Spring annotations like @NotNull, @Size, @Email, and @Pattern.
UI Design
Add/Edit User Form: Input fields for user details, with validation error messages displayed.
User List: Displays users in a table with options for editing and deleting.
Validation Feedback: Error messages shown under respective fields.
Testing Strategy
Unit Tests: Validate input rules using Spring Boot's testing framework.
Integration Tests: Test full workflow: form submissions, database interactions, CRUD operations.
User Acceptance Testing: Ensure functionality meets user needs.
Error Handling
Display user-friendly messages for invalid inputs.
Handle common exceptions and display custom error pages.
Deployment
The application can be deployed locally or on a remote server using:

Embedded Tomcat (provided by Spring Boot)
Conclusion
This project follows best practices for building a scalable, maintainable, and user-friendly web application using Spring Boot, Spring Data JPA, Lombok, and Thymeleaf.
