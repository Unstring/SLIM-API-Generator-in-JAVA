# PHP Slim API CRUD Generator

A powerful Java-based desktop application that automatically generates a complete PHP Slim API with CRUD operations, authentication, and proper API versioning from your MySQL database schema.

## Features

- **Database Integration**
  - Connects to MySQL database
  - Automatically maps database tables to API endpoints
  - Supports relationships and complex schemas

- **API Generation**
  - Generates RESTful API endpoints with CRUD operations
  - Implements proper API versioning (/api/v1/...)
  - Creates route groups for better organization
  - Supports authentication and protected routes

- **Authentication**
  - JWT-based authentication
  - Configurable auth table and fields
  - Protected routes with middleware
  - User registration and login endpoints

- **Code Structure**
  - MVC architecture (Models, Controllers, Services)
  - Clean code separation
  - Proper namespacing
  - PSR-4 autoloading

## Prerequisites

Before running the generator, ensure you have:

- Java Development Kit (JDK) 17 or higher
- MySQL database server
- PHP 7.3 or higher
- Composer (PHP package manager)

## Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Unstring/SLIM-API-Generator-in-JAVA.git
   ```

2. Build the project:
   ```bash
   mvn clean install
   ```

3. Run the generator:
   ```bash
   java -jar target/crud-generator.jar
   ```

## Using the Generated API

1. Navigate to your generated project directory:
   ```bash
   cd your-package-name
   ```

2. Install PHP dependencies:
   ```bash
   composer install
   ```

3. Start the development server:
   ```bash
   composer start
   ```
   Your API will be available at `http://localhost:8080`

## Project Requirements

### For Generator
- JDK 17 or higher
- Maven
- MySQL Server

### For Generated API
- PHP 7.3 or higher
- Composer
- MySQL Server
- Required PHP Extensions:
  - php-mysql
  - php-json
  - php-mbstring

## Dependencies Used

### Java Dependencies
- Java Swing (GUI)
- MySQL Connector/J
- Google Guava

### PHP Dependencies
```json
{
    "require": {
        "php": ">=7.3",
        "slim/slim": "4.13.0",
        "slim/psr7": "^1.3",
        "php-di/php-di": "^6.3",
        "php-di/slim-bridge": "^3.4",
        "illuminate/database": "^10.48",
        "firebase/php-jwt": "^6.1",
        "vlucas/phpdotenv": "^5.6",
        "selective/basepath": "^2.0"
    }
}
```

## Generated Structure

The CRUD Generator creates the following code structure:

- PHP Slim Controllers:
  - `[TableName]Controller.php`: Controller for handling API endpoints for the table.

- PHP Models:
  - `[TableName].php`: Model class representing the table structure.

- PHP Services:
  - `[TableName]Service.php`: Service class for handling business logic and database operations.

- Routes:
  - `api.php`: Slim framework routes configuration for the generated endpoints.

- .env File:
  - `.env`: Environment configuration file for database and application settings.

## Dependencies

The CRUD Generator utilizes the following dependencies:

- Java Swing: For creating the GUI components.
- MySQL Connector/J: For connecting to the MySQL database.
- Regex: For processing and manipulating table and column names.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

The PHP Slim API CRUD Generator was developed by [Lance](https://www.lance.name).

## Project Structure

```
your-package-name/
├── app/
│   ├── Controllers/
│   │   ├── AuthController.php
│   │   └── [TableName]Controller.php
│   ├── Models/
│   │   └── [TableName].php
│   ├── Services/
│   │   ├── AuthService.php
│   │   └── [TableName]Service.php
│   └── Middleware/
│       └── AuthMiddleware.php
├── routes/
│   └── api.php
├── public/
│   └── index.php
├── .env
└── composer.json
```

## API Endpoints

### Authentication Endpoints
```
POST /api/v1/auth/register
POST /api/v1/auth/login
GET  /api/v1/[auth-table]/me    (Protected)
```

### Resource Endpoints
For each table, the following endpoints are generated:
```
GET    /api/v1/[table]          - List all records
GET    /api/v1/[table]/{id}     - Get single record
POST   /api/v1/[table]          - Create new record
PUT    /api/v1/[table]/{id}     - Update record
DELETE /api/v1/[table]/{id}     - Delete record
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Developed by [Amit Anand](https://github.com/Unstring) - A passionate developer who's always learning!

## Links

- [GitHub Repository](https://github.com/Unstring/SLIM-API-Generator-in-JAVA)
- [Report Issues](https://github.com/Unstring/SLIM-API-Generator-in-JAVA/issues)
- [ORCID](https://orcid.org/0009-0009-3022-093X)

## Support

If you find this project helpful, consider:
- Giving it a star ⭐ on GitHub
- Contributing to its development
- Reporting issues or suggesting improvements
- Sharing it with others who might find it useful

---

Made with ❤️ by [@Unstring](https://github.com/Unstring)
