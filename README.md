# ONLINE-ART-GALLERY-MANAGEMENT-SYSTEM
Online Art Gallery Management System

An Online Art Gallery Management System is a web-based application developed using PHP and MySQL that allows art galleries to manage and display artwork online. The system provides separate functionality for administrators and users, making it easier to manage artworks, artists, categories, users, and online purchases.

Features
Admin Features
Secure admin login and logout
Dashboard with system statistics
Add, edit, and delete artworks
Manage artwork categories
Manage artist information
Upload artwork images
View registered users
Manage customer orders
View and update order status
Manage gallery information
View contact and user enquiries
User Features
User registration and login
Browse available artworks
Search for artworks
Filter artworks by category
View artwork details
View artist information
Add artworks to cart
Place orders
View order history
Manage user profile
Contact the gallery
Technologies Used
Frontend: HTML5, CSS3, JavaScript, Bootstrap
Backend: PHP
Database: MySQL
Server: Apache
Development Environment: XAMPP / WAMP
Browser: Chrome, Firefox, Edge, or any modern web browser
Project Structure
Online-Art-Gallery/
│
├── admin/
│   ├── dashboard.php
│   ├── artworks.php
│   ├── add-artwork.php
│   ├── edit-artwork.php
│   ├── artists.php
│   ├── categories.php
│   ├── users.php
│   └── orders.php
│
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
│
├── config/
│   └── database.php
│
├── includes/
│   ├── header.php
│   ├── footer.php
│   └── auth.php
│
├── uploads/
│   └── artworks/
│
├── index.php
├── artworks.php
├── artwork-details.php
├── artists.php
├── cart.php
├── checkout.php
├── login.php
├── register.php
├── profile.php
├── orders.php
└── contact.php


The exact folder structure may vary depending on your implementation.

Requirements

Before installing the project, make sure the following software is installed:

PHP 7.4 or later
MySQL 5.7 or later
Apache Server
XAMPP, WAMP, or another PHP development environment
Web browser
Installation
1. Download the Project

Download or clone the project source code and place it inside your web server directory.

For XAMPP:

C:\xampp\htdocs\


For example:

C:\xampp\htdocs\Online-Art-Gallery\

2. Start XAMPP

Open the XAMPP Control Panel and start:

Apache
MySQL
3. Create the Database

Open phpMyAdmin in your browser:

http://localhost/phpmyadmin


Create a new database, for example:

online_art_gallery

4. Import the Database

Import the provided SQL file into the newly created database.

For example:

database/online_art_gallery.sql


If your project does not include an SQL file, create the required tables manually according to your PHP code.

5. Configure Database Connection

Open the database configuration file:

config/database.php


Update the database credentials:

<?php

$host = "localhost";
$username = "root";
$password = "";
$database = "online_art_gallery";

$conn = mysqli_connect($host, $username, $password, $database);

if (!$conn) {
    die("Database connection failed: " . mysqli_connect_error());
}
?>


Change the username, password, host, or database name if your MySQL configuration is different.

6. Run the Project

Open your browser and visit:

http://localhost/Online-Art-Gallery/


The application should now be available.

Database Modules

The system can contain the following main database tables:

Table	Purpose
users	Stores registered user information
admins	Stores administrator accounts
artists	Stores artist information
categories	Stores artwork categories
artworks	Stores artwork details
cart	Stores items added to the shopping cart
orders	Stores customer orders
order_items	Stores individual items within orders
contacts	Stores user enquiries
Main Modules
Authentication Module

Provides registration and login functionality for users and administrators. Passwords should be securely hashed before being stored in the database.

Artwork Management

Administrators can add new artworks with information such as:

Artwork title
Artist
Category
Description
Price
Image
Availability
Artist Management

Administrators can create and maintain artist profiles containing information such as the artist's name, biography, and profile image.

Category Management

Artworks can be organized into categories such as:

Paintings
Digital Art
Photography
Sculptures
Abstract Art
Traditional Art
Shopping Cart

Users can add available artworks to their cart, modify quantities where applicable, remove items, and proceed to checkout.

Order Management

Users can view their orders and order status. Administrators can review orders and update their status.

Security

For production deployment, the following security practices are recommended:

Use password hashing with password_hash().
Verify passwords using password_verify().
Use prepared SQL statements to prevent SQL injection.
Validate and sanitize user input.
Restrict access to administrator pages.
Validate uploaded image files.
Limit permitted file types and file sizes.
Store sensitive configuration outside publicly accessible directories where possible.
Use HTTPS in production.
Regenerate sessions appropriately after authentication.
Example Password Hashing
$passwordHash = password_hash($password, PASSWORD_DEFAULT);


To verify a password:

if (password_verify($password, $passwordHash)) {
    // Login successful
}

Future Enhancements

The project can be extended with:

Online payment gateway integration
Wishlist functionality
Artwork reviews and ratings
Artist verification
Email notifications
Advanced artwork search
Image zoom and gallery views
Sales reports and analytics
Invoice generation
Multiple administrator roles
Responsive mobile application
Cloud image storage
Advantages
Provides an online platform for displaying artwork.
Reduces manual gallery management.
Allows customers to browse artworks from anywhere.
Makes artwork and artist information easy to manage.
Simplifies order management.
Provides a centralized database for gallery information.
License

This project is intended for educational and academic purposes. You may modify and extend the source code according to your project requirements.

Author

Online Art Gallery Management System

Developed using PHP, MySQL, HTML, CSS, JavaScript, and Bootstrap.
