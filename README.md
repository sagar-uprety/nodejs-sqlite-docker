# Node.js Sample Demo App

This is a Node.js application that uses SQLite as the default database. It's a simple todo list tracker with a UI to perform CRUD operations. If MySQL is available, the application can be configured to use MySQL instead.

## Prerequisites

- Node.js
- npm (Node Package Manager)
- Docker (optional)
- Docker Compose (optional)

## Installation and Running Locally

1. Clone the repository:
    ```sh
    git clone https://github.com/sagar-uprety/nodejs-sqlite-docker.git
    ```
2. Navigate to the project directory:
    ```sh
    cd nodejs-sqlite-docker
    ```
3. Install the dependencies:
    ```sh
    npm install
    ```
    
## Configuration

### SQLite (default)

No additional configuration is needed for SQLite. The application will use SQLite by default.
The database file will be created in the database directory inside the project i.e ```./database/todo.db```

### MySQL (optional)

If you want to use MySQL instead, you need to set up the database and update the configuration file:

1. Create a MySQL database and user.
2. Update the `.env` file with your MySQL credentials:
    ```env
    MYSQL_HOST: insert-value-here,
    MYSQL_HOST_FILE: insert-value-here,
    MYSQL_USER: insert-value-here,
    MYSQL_USER_FILE: insert-value-here,
    MYSQL_PASSWORD: insert-value-here,
    MYSQL_PASSWORD_FILE: insert-value-here,
    MYSQL_DB: insert-value-here,
    MYSQL_DB_FILE: insert-value-here
    ```

## Usage

### Running with Node.js

To start the application, run:
```sh
npm start
```
```sh
nodemon index.js # in development
```

### Running with Docker

To run the application using Docker, follow these steps:

1. Build the Docker image:
    ```sh
    docker build -t nodejs-app .
    ```

2. Run the Docker container:
    ```sh
    docker run -p 3000:3000 nodejs-app
    ```

The application will be accessible at `http://localhost:3000`.

### Running with Docker Compose

To run the application using Docker Compose, run the following:

    ```sh
    docker-compose up
    ```

The application will be accessible at `http://localhost:3000`.

To stop the application, use:
```sh
docker-compose down
```

## Contributing

1. Fork the repository.
2. Create a new branch:
    ```sh
    git checkout -b feature-branch
    ```
3. Make your changes.
4. Commit your changes:
    ```sh
    git commit -m 'Add some feature'
    ```
5. Push to the branch:
    ```sh
    git push origin feature-branch
    ```
6. Open a pull request.

## License

This project is licensed under the MIT License.
