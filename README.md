# Flask REST API - User Management
This project is part of a Python Developer Internship Task 4.
The objective is to build a simple REST API using Flask that manages user data with basic CRUD operations.

## Features
- GET → Fetch all users or a specific user
- POST → Add a new user
- PUT → Update user details
- DELETE → Remove a user
- In-memory storage (dictionary) used instead of a database

## Tech Stack
- Python 3
- Flask
- Postman / Curl (for testing)

## Setup & Installation
- Clone the repository:
  ```bash
  git clone <your-repo-link>
  cd flask_user_api
- Install dependencies:
  ```bash
  pip install -r requirements.txt
- Run the app:
  ```bash
  python app.py
- The app will run on: http://127.0.0.1:5000

## API Endpoints
1. Home
 GET /
- Response:
{"message": "Welcome to the User API!"}
2. Get All Users
- GET /users
3. Get Single User
- GET /users/<user_id>
4. Create User
- POST /users
- Body (JSON):
{
  "name": "Alice",
  "email": "alice@example.com"
}
5. Update User
- PUT /users/<user_id>
Body (JSON):
{
  "email": "newalice@example.com"
}
6. Delete User
- DELETE /users/<user_id>

## Example with Curl
- curl -X POST http://127.0.0.1:5000/users \
-H "Content-Type: application/json" \
-d '{"name":"Alice","email":"alice@example.com"}'

## Key Learnings
- Basics of Flask API development
- REST principles & HTTP methods
- JSON handling with Flask
- Testing APIs using Postman / Curl

## Future Improvements
- Use a database (SQLite / PostgreSQL) instead of in-memory dictionary
- Add authentication (JWT tokens)
- Add pagination and filtering for users
