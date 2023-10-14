# PERN-Todo

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Database Setup](#database-setup)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Testing with Postman](#testing-with-postman)
- [Contributing](#contributing)

## Introduction

Welcome to the PERN (PostgreSQL, Express, React, Node.js) stack todo application! This project is a simple todo list application built using the PERN stack. 
It allows users to create, update, and delete tasks.

## Features

- Create new tasks with a title and description.
- Update task details.
- Delete tasks.

## Prerequisites

Before you get started, ensure you have the following prerequisites installed:

- Node.js and npm
- PostgreSQL (Make sure you have a PostgreSQL database set up)
- Git (for cloning the project)

## Database Setup

1. Open a PostgreSQL client (e.g., `psql`) and connect to your PostgreSQL server.

2. Create a new database for the project (assuming you haven't already done this):
   ```sql
   CREATE DATABASE perntodo;
   ```

3. Switch to the newly created database:
   ```sql
   \c perntodo;
   ```

4. Create a table to store todo items (you can use the provided SQL statement):
   ```sql
   CREATE TABLE todo (
       todo_id SERIAL PRIMARY KEY,
       description VARCHAR(255)
   );
   ```

5. Ensure your database credentials match the configuration in your `.env` file.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/BettyyN/PERN-Todo.git
   ```

2. Change to the project directory:
   ```bash
   cd your-project-directory
   ```

3. Install the project dependencies:
   ```bash
   npm install
   ```

4. Configure your PostgreSQL database connection by editing the `.env` file with your database credentials:
   ```env
   DB_USER=postgres
   DB_PASSWORD=1234
   DB_HOST=localhost
   DB_PORT=5432
   DB_DATABASE=perntodo
   ```

## Running the Application

To run the PERN stack application, use the following command:

```bash
npm start
```

The server will start at `http://localhost:5000` and the client at `http://localhost:3000`. The application uses the default ports for development, but you can configure them in the `.env` file if needed.

## API Endpoints

The API endpoints for this project include:

- `GET /api/todos`: Get a list of all todos.
- `GET /api/todos/:id`: Get a specific todo by ID.
- `POST /api/todos`: Create a new todo.
- `PUT /api/todos/:id`: Update a todo by ID.
- `DELETE /api/todos/:id`: Delete a todo by ID.

## Testing with Postman

You can use Postman to test the API endpoints. Import the provided `pern-stack-todo.postman_collection.json` collection file into Postman to get started. Make sure the server is running locally while testing.

## Contributing

Contributions to this project are welcome. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push to your fork and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

This README provides instructions for setting up the PostgreSQL database and the associated table, as well as integrating it with your PERN stack todo application. Make sure to adjust it according to your project's structure and requirements.
