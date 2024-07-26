# FastAPI Blog Application

This repository contains a FastAPI application for managing blogs and users. The application includes features for creating, reading, updating, and deleting blog posts, as well as user authentication and JWT-based authorization.

## Features

- **Blog Management**: Create, read, update, and delete blog posts.
- **User Management**: Create and retrieve user information.
- **Authentication**: User login with JWT token generation and validation.

## Endpoints

### Blogs

- `GET /blog/`: Retrieve all blog posts.
- `POST /blog/`: Create a new blog post.
- `DELETE /blog/{id}`: Delete a blog post by ID.
- `PUT /blog/{id}`: Update a blog post by ID.
- `GET /blog/{id}`: Retrieve a blog post by ID.

### Users

- `POST /user/`: Create a new user.
- `GET /user/{id}`: Retrieve user information by ID.

### Authentication

- `POST /login`: User login to generate JWT token.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/fastapi-blog-application.git
    cd fastapi-blog-application
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Running the Application

1. Start the FastAPI application:
    ```bash
    uvicorn main:app --reload
    ```

2. Open your browser and navigate to `http://127.0.0.1:8000/docs` to access the API documentation.

## Project Structure

- `main.py`: The main application entry point.
- `models.py`: SQLAlchemy models for the database.
- `schemas.py`: Pydantic models for request and response validation.
- `database.py`: Database connection setup.
- `routers/`: Directory containing the routers for different endpoints.
- `repository/`: Directory containing the repository functions for database operations.
- `hashing.py`: Utility functions for hashing passwords.
- `token.py`: Functions for creating and verifying JWT tokens.

## Dependencies

- FastAPI
- Uvicorn
- SQLAlchemy
- Passlib
- Bcrypt
- PyJWT

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
