# JWT-Auth

A simple JWT-based authentication system implemented in Go.

## Project Structure

```bash
JWT-AUTH/
├── controllers/
│   ├── usersController.go     # Controller for user-related actions
├── initializers/
│   ├── connectToDb.go         # Database connection setup
│   ├── loadEnvVariables.go    # Load environment variables
│   ├── syncDatabase.go        # Sync database schema
├── middleware/
│   ├── requireAuth.go         # Middleware for authentication
├── models/
│   ├── userModel.go           # User model definition
├── .env                       # Environment variables
├── .gitignore                 # Git ignore file
├── go.mod                     # Go module file
├── go.sum                     # Go dependencies file
├── main.go                    # Main entry point of the application
├── readme.md                  # Project documentation
├── test.db                    # Test database file
```

## Getting Started

### Prerequisites

- Go 1.16 or higher
- A running instance of a SQL database (e.g., PostgreSQL, MySQL, SQLite)

#### Packages
- https://github.com/golang-jwt/jwt
- https://github.com/joho/godotenv
- https://pkg.go.dev/golang.org/x/crypto#section-readme
- https://gin-gonic.com/docs/
- https://gorm.io/docs/

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/thrtn85/jwt-auth.git
   cd jwt-auth
   ```

2. Install dependencies:
   ```bash
   go mod download
   ```

3. Set up your environment variables:
   ```bash
   cp .env.example .env
   # Update .env with your database credentials and other configurations
   ```

4. Initialize the database:
   ```bash
   go run initializers/syncDatabase.go
   ```

### Running the Application

To run the application, use:
```bash
go run main.go
```

### Project Structure Overview

- **controllers/**: Contains the controllers for handling HTTP requests.
- **initializers/**: Contains the initialization scripts for setting up the database and loading environment variables.
- **middleware/**: Contains middleware functions for request processing.
- **models/**: Contains the data models used in the application.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.