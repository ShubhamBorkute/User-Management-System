# User Management System

## Project Overview
This project is a **User Management System** that allows performing CRUD (Create, Read, Update, Delete) operations to manage user details like:
- First Name
- Last Name
- Phone Number
- Email ID
- Address

## Features
- **CRUD Operations**: Manage user data (add, view, update, delete).
- **Data Validation**: Ensure correct user input on both client and server sides.
- **Responsive UI**: User-friendly interface for managing user details.
- **Persistent Storage**: Store user data in a MySQL database.

## Technology Stack

### Backend
- **Spring Boot**: Java-based backend framework for building RESTful APIs.
- **Spring Data JPA**: ORM for database operations.
- **Spring Validation**: For validating user inputs.

### Frontend
- **Thymeleaf**: Template engine for rendering dynamic HTML.
- **HTML5/CSS3**: For UI structure and styling.
- **JavaScript**: Optional client-side interactions.

### Database
- **MySQL**: Relational database used for storing user data.

## System Design
The project follows the **MVC (Model-View-Controller)** architecture:
- **Model**: Represents the user entity and database interaction.
- **View**: Thymeleaf templates for UI.
- **Controller**: Manages HTTP requests and routes them to the appropriate services.

### Components
- **UserEntity**: Defines the user fields (first name, last name, phone number, etc.).
- **UserRepository**: Handles CRUD operations using Spring Data JPA.
- **UserController**: Handles incoming requests and user actions.

## Database Schema
### User Table
| Field         | Type     | Constraints                                  |
| ------------- | -------- | -------------------------------------------- |
| `id`          | Integer  | Primary Key, Auto-Increment                  |
| `first_name`  | String   | Not Null, 2-30 characters                    |
| `last_name`   | String   | Not Null, 2-30 characters                    |
| `phone`       | String   | Not Null, Unique, 10 digits                  |
| `email`       | String   | Not Null, Unique, Valid Email Format         |
| `address`     | String   | Not Null, 5-100 characters                   |

## Functionalities
1. **Add User**: Users can input their details and submit them.
2. **View Users**: Display all users with options to update or delete.
3. **Update User**: Users can update their information.
4. **Delete User**: Remove a user from the system after confirmation.

## Validation Rules
- **First Name/Last Name**: 2-30 characters, not null.
- **Phone Number**: Must be exactly 10 digits.
- **Email ID**: Must be a valid email format.
- **Address**: 5-100 characters, not null.

## Non-Functional Requirements
- **Data Validation**: Client-side via HTML5 attributes and server-side via Spring Validation.
- **Security**: Basic security measures against common attacks like SQL injection.
- **Performance**: Efficient database operations with Spring Data JPA.

## Testing
- **Unit Tests**: Validate business logic and input validation.
- **Integration Tests**: Ensure proper functioning of CRUD operations and database interaction.
- **User Acceptance Testing**: Ensure the UI and system meet user expectations.

## Deployment
The project can be deployed locally or remotely using an embedded **Tomcat server** with Spring Boot.

## License
This project is licensed under the MIT License.
