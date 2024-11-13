# User Authentication System with JWT and FastAPI

This project implements a user authentication system using **JWT (JSON Web Tokens)** with **FastAPI** and **MongoDB**. The application allows secure login, logout, and user CRUD operations. This system is designed with scalability in mind, making it easy to extend or modify for future needs.

## Features

### Must-Have
1. **Login and Logout Endpoints**: Users can log in to receive a JWT token and use it for authentication.
2. **Secure User CRUD Endpoints**: All user CRUD operations (create, read, update, delete) are secure and accessible only to authenticated users.
3. **Readable Code**: Code is structured for readability and maintenance.
4. **No ODM Library**: Direct MongoDB operations without using ODM libraries like Odmantic or Beanie.
5. **User Creation Script**: A script is included to create users in a predefined MongoDB database and collection.

### Good-to-Have
1. **Logging**: Adds logging across the API to trace operations and errors.
2. **Predefined Models**: Uses Pydantic models for user and token, providing validation and documentation support.
3. **MongoDB Atlas**: Option to connect to MongoDB Atlas for cloud-based database hosting.
4. **Scalable Structure**: Code is modularized to support potential extensions or scaling.

### Added Bonus
1. **Role-Based Access Control (RBAC)**: Implementing RBAC for different user roles (e.g., Admin, User).
2. **Deployment**: Deploy the service to a serverless platform like Heroku, Vercel, or any other free service.

---

## Setup and Installation

### Prerequisites
- Python 3.7+
- MongoDB (or MongoDB Atlas for cloud support)
- [FastAPI](https://fastapi.tiangolo.com/)
- [Uvicorn](https://www.uvicorn.org/)
- [PyMongo](https://pymongo.readthedocs.io/)
- [Python dotenv](https://pypi.org/project/python-dotenv/) for environment variable management

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Ajayraj1515/user_authentication_system.git
   cd user_authentication_system
### Install Dependencies   
pip install -r requirements.txt
### Environment Variables Create a .env file in the root directory with the following keys:
SECRET_KEY=your_secret_key
MONGO_URI=mongodb://localhost:27017
### Replace MONGO_URI with your MongoDB connection string if using MongoDB Atlas.

### Run the Application

uvicorn main:app --reload

Access the API Documentation Open http://127.0.0.1:8000/docs to view the automatically generated API documentation.


### API Endpoints
Authentication
POST /login: Authenticates the user and returns a JWT token.
POST /logout: Logs out the user (placeholder endpoint).
User CRUD (Requires Authentication)
POST /users/: Create a new user.
GET /users/me: Retrieve the authenticated user’s details.
GET /users/{username}: Retrieve details of a specific user.
PUT /users/{username}: Update user information.
DELETE /users/{username}: Delete a user.


### RBAC and Future Improvements
Role-Based Access Control (RBAC): Add roles like Admin and User with restricted access to certain routes.
Deployment: Deploy the API on a serverless platform or cloud service for accessible endpoints.
Logging: Add structured logging to enhance traceability and debugging.
Tests: Implement unit and integration tests for enhanced reliability.
