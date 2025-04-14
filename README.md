# Travel Booking System (TBS)

A Java desktop application for managing travel bookings, packages, and user accounts.

## Features

- User authentication and registration
- Browse and search travel packages
- Book travel packages
- View and cancel bookings
- Admin functionality for managing packages and users

## Technologies Used

- Java
- Swing for GUI
- MySQL for database storage
- JDBC for database connectivity

## Prerequisites

- JDK 8 or higher
- MySQL Server 5.7 or higher
- MySQL Connector/J (JDBC driver)

## Setup Instructions

### 1. Database Setup

1. Install MySQL Server if not already installed
2. Create a new database named `tbs`
3. Import the provided SQL schema from `database/tbs_schema.sql`

```mysql -u root -p
<Enter your password>
SOURCE database/tbs_schema.sql;
```

### 2. Configure Database Connection

1. Navigate to the `config` directory
2. Copy `db.properties.example` to `db.properties`
3. Edit `db.properties` and update with your MySQL credentials:

```properties
db.url=jdbc:mysql://localhost:3306/tbs
db.user=your_username
db.password=your_password
```

### 3. Compile and Run the Application

#### Using an IDE (Eclipse, IntelliJ IDEA, etc.)

1. Import the project into your IDE
2. Download and the MySQL JDBC connector to your project's classpath or 'lib' directory
3. Run the `App.java` file as the main class

#### Using Command Line

1. Navigate to the project root directory
2. Compile the Java files:

```bash
javac -d bin -cp lib/mysql-connector-java.jar src/*.java src/**/*.java
```

3. Run the application:

```bash
java -cp bin:lib/mysql-connector-java.jar App
```

For Windows, use `;` instead of `:` in the classpath:

```bash
java -cp bin;lib/mysql-connector-java.jar App
```

## Project Structure

```
TBS/
├── src/                  # Source code
│   ├── db/               # Database connection code
│   ├── exception/        # Custom exceptions
│   ├── model/            # Data models
│   ├── service/          # Business logic
│   ├── ui/               # User interface
│   ├── utils/            # Utility classes
│   └── App.java          # Main application entry
├── config/               # Configuration files
│   └── db.properties     # Database configuration (not in git)
├── database/             # SQL scripts
│   └── tbs_schema.sql    # Database schema
├── lib/                  # External libraries/dependencies
└── README.md             # This file
```

## Usage

1. **Login Screen**: Enter credentials or register a new account
2. **Home Page**: Browse available travel packages
3. **Package Details**: View detailed information and book packages
4. **My Bookings**: View and manage your bookings

## License

This project is for educational purposes only. Not for commercial use.