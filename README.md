# PG Room Management System

A simple PHP-based web application for managing a paying guest (PG) accommodation system. The project supports two roles:

- Admin for managing rooms, users, allocations, payments, complaints, and reviews
- User for viewing profile, room details, payment history, and submitting complaints/reviews

## Features

### Admin Panel
- Dashboard with key statistics
- Manage users
- Add, edit, and delete rooms
- Allocate rooms to tenants
- Track payments
- Manage complaints and review submissions
- View room allocation records

### User Panel
- Login and session-based access
- View profile
- View assigned room details
- View payment history
- Raise complaints
- Add or update reviews
- Change password

## Tech Stack

- PHP
- MySQL
- HTML/CSS/JavaScript
- Bootstrap-like custom styling with Font Awesome icons
- Apache server via XAMPP/WAMP

## Project Structure

```text
PG_Room_Management_System/
├── admin/                  # Admin pages and management modules
├── user/                   # User dashboard and user-side functionality
├── includes/               # Shared DB/session/header/sidebar files
├── css/                    # Stylesheets
├── js/                     # Frontend scripts
├── database/               # SQL scripts
├── images/                 # Image assets
├── index.php               # Redirect entry point
├── login.php               # Login page for admin and users
├── includes/db.php         # Database connection file
├── README.md               # Project documentation
└── README.txt              # Additional notes placeholder
```

## Prerequisites

Before running this project, make sure you have:

- XAMPP or WAMP installed
- Apache and MySQL running
- PHP 7+ (or compatible version)
- A web browser

## Setup Instructions

1. Clone or download this project into your local web server directory.

   Example for XAMPP:

   ```bash
   C:\xampp\htdocs\Pg_Room_Management_System
   ```

2. Start Apache and MySQL from XAMPP Control Panel.

3. Create a MySQL database named:

   ```sql
   pg_room_management
   ```

4. Import the database script from the `database` folder (if available in your environment).

5. Open `includes/db.php` and confirm the database connection settings:

   ```php
   $servername = "localhost";
   $username = "root";
   $password = "";
   $database = "pg_room_management";
   ```

6. Open the application in the browser:

   ```text
   http://localhost/Pg_Room_Management_System/
   ```

7. Login using the admin or user credentials available in your database.

## Default Login Flow

- The `login.php` file checks the credentials in two tables:
  - `admin`
  - `users`
- Admin users are redirected to the admin dashboard.
- Normal users are redirected to the user dashboard.

## Database Notes

This project expects MySQL tables such as:

- `admin`
- `users`
- `rooms`
- `room_allocation`
- `payments`
- `complaints`
- `reviews`

If your database is empty, create the required tables and seed the necessary admin/user records before using the application.

## Development Notes

- The project uses direct PHP + MySQL queries without a framework.
- Session-based authentication is used for admin and user access.
- Pages are organized by role to keep admin and user features separated.

## License

This project is intended for learning and local development purposes.

## Author

PG Room Management System
