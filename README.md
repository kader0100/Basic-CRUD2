# PHP CRUD with PDO and MySQL

This project is a simple PHP CRUD (Create, Read, Update, Delete) application using PDO for secure database interactions. It includes a MySQL database, a user-friendly interface with Bootstrap, and essential features for managing user records.

## Features
- Uses **PDO** for secure database interaction.
- Implements **Create, Read, Update, and Delete (CRUD)** operations.
- Simple UI with **Bootstrap** for styling.
- Database connection handled via `db.php`.

## Requirements
- PHP 7.4+ or PHP 8+
- MySQL Database
- Web server (Apache, Nginx, or built-in PHP server)

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/kader0100/Basic-CRUD2.git
cd Basic-CRUD2 
```

### 2. Setup Database
- Create a MySQL database and import the provided SQL file:
```sql
CREATE DATABASE test_db;
USE test_db;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL
);

INSERT INTO users (name, email) VALUES
('John Doe', 'john@example.com'),
('Jane Smith', 'jane@example.com'),
('Alice Johnson', 'alice@example.com');
```

### 3. Configure Database Connection
- Open `db.php` and modify the database credentials if needed:
```php
$dsn = 'mysql:host=localhost;dbname=test_db;charset=utf8mb4';
$username = 'root';
$password = '';
```

### 4. Run the Application
#### Using PHP Built-in Server
- Start a PHP built-in server (or use Apache/Nginx):
```sh
php -S localhost:8000
```
- Open your browser and go to:
```
http://localhost:8000/index.php
```

#### Using Laragon or LAMP Server
- **Laragon**:
  1. Place the project folder inside `C:\laragon\www\`
  2. Start Laragon and click **Start All**
  3. Open a browser and go to:
     ```
     http://localhost/Basic-CRUD2/index.php
     ```

- **LAMP (Linux, Apache, MySQL, PHP)**:
  1. Move the project folder to `/var/www/html/`
  2. Restart Apache:
     ```sh
     sudo systemctl restart apache2
     ```
  3. Open a browser and go to:
     ```
     http://localhost/Basic-CRUD2/index.php
     ```

## File Structure
```
php-crud-pdo/
│── db.php         # Database connection
│── index.php      # List all users
│── create.php     # Add a new user
│── update.php     # Edit user details
│── delete.php     # Delete a user
│── README.md      # Project Documentation
```

## Usage
- **Add User**: Click "Add User", enter details, and submit.
- **Edit User**: Click "Edit" next to a user, modify details, and update.
- **Delete User**: Click "Delete" to remove a user (confirmation required).

## License
This project is open-source and available under the GPL-3.0 license.

---
Happy coding! 🚀

