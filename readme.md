# NodeAuth

## Overview
This project is a simple authentication service built with Node.js, Express, MongoDB, and JWT authentication. It provides user registration, login, and authentication middleware for protected routes.

## Features
- User registration with encrypted passwords
- User login with JWT authentication
- Middleware to protect routes
- Simple frontend for testing authentication
- API endpoints for authentication
- Token-based authentication with JWT
- Secure password hashing with bcrypt
- CORS support for cross-origin requests

## Technologies Used
- Node.js
- Express.js
- MongoDB with Mongoose
- JSON Web Token (JWT)
- bcrypt for password hashing
- CORS and Morgan for middleware
- dotenv for environment variables

## Installation

### 1. Clone the repository
```sh
git clone https://github.com/AmirMohammedi/NodeAuth.git
cd NodeAuth
```

### 2. Install dependencies
```sh
npm install
```

### 3. Create a `.env` file and configure environment variables
```sh
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
```

### 4. Run the server
```sh
npm run dev
```

The server will start on `http://localhost:5000`

## API Endpoints

### **1. Register a new user**
- **Endpoint:** `POST /api/auth/register`
- **Request Body:**
```json
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "123456"
}
```
- **Response:**
```json
{
  "message": "User registered successfully"
}
```

### **2. Login**
- **Endpoint:** `POST /api/auth/login`
- **Request Body:**
```json
{
  "email": "test@example.com",
  "password": "123456"
}
```
- **Response:**
```json
{
  "token": "your_generated_jwt_token"
}
```

### **3. Access a Protected Route**
- **Endpoint:** `GET /api/protected`
- **Headers:**
```sh
Authorization: Bearer your_generated_jwt_token
```
- **Response:**
```json
{
  "message": "Protected content"
}
```

## Testing with Postman
1. Use `POST /api/auth/register` to create a user.
2. Use `POST /api/auth/login` to log in and receive a token.
3. Use the token to access protected routes.

## Contribution
Feel free to fork the repository and submit pull requests.

## License
This project is open-source and available for use and modification.

