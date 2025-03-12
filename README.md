# AWS Image Upload Application

This is a Spring Boot application that allows users to upload and manage customer profiles, including profile images, using Amazon S3 for storage. The application also includes authentication and authorization using JWT (JSON Web Tokens). A React-based frontend is also available for interacting with the application.

## Features

- **Customer Management**: Create, read, update, and delete customer profiles.
- **Profile Image Upload**: Upload and retrieve customer profile images stored in Amazon S3.
- **Authentication**: Secure login and registration with JWT-based authentication.
- **Authorization**: Role-based access control for different endpoints.
- **RESTful API**: Exposes endpoints for managing customers and their profile images.
- **Frontend Integration**: React frontend that enables user interaction with the backend.

## Technologies Used

### Backend
- **Spring Boot**: Core framework for building the application.
- **Spring Security**: Handles authentication and authorization.
- **JWT (JSON Web Tokens)**: Used for secure authentication.
- **Amazon S3**: Storage service for customer profile images.
- **PostgreSQL**: Database for storing customer information.
- **Lombok**: Reduces boilerplate code with annotations.
- **AWS SDK for Java**: Integrates with Amazon S3 for file storage.

### Frontend
- **React.js**: JavaScript library for building the user interface.
- **Vite**: Development server and build tool.
- **Axios**: HTTP client for making API requests.

## Getting Started

### Prerequisites

- Java 21
- Maven
- PostgreSQL
- AWS account with an S3 bucket configured
- Node.js (for the frontend)

### Frontend Installation

1. **Navigate to the frontend directory**:
   ```bash
   cd frontend/react
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Run the frontend application**:
   ```bash
   npm start
   ```

4. **Access the frontend**:
   - Open a browser and navigate to `http://localhost:5173`.
   - Sign up and log in.
   - Once logged in, add customers.
   - Customers can log in and update their profiles.
   - When updating, users can upload profile images, which are stored in the AWS S3 bucket.
   - 
## Security

- **Authentication**: JWT-based authentication secures the endpoints.
- **Authorization**: Only authenticated users can access certain endpoints.
- **CORS**: Configured to allow requests from any origin.

## Configuration

The application configuration is managed via the `application.yml` file. Key configurations include:

- **Database**: PostgreSQL connection details.
- **AWS S3**: AWS region and S3 bucket name.
- **JWT**: Secret key for signing JWT tokens.
- **CORS**: Allowed origins, methods, and headers.
