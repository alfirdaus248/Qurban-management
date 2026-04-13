# Qurban Management System

## Overview

The Qurban Management System is a web-based application developed to manage the qurban process within a community. The system handles citizen data, role assignment, meat distribution, financial transactions, and QR-based verification for meat collection.

This application is designed to simplify and organize real-world qurban activities in a structured and efficient way.

## Features

User and Role Management

* Multi-role system: Warga, Panitia, Berqurban, Admin
* One user can have multiple roles
* Role-based access control

Dashboard

* Admin dashboard with statistics: total citizens, panitia, qurban participants
* Financial summary: total income, expenses, and balance
* User dashboard displaying personal QR code and role information

Meat Distribution System

* Automatic meat allocation based on role
  Warga: 2 kg
  Panitia: 2 kg
  Berqurban: 4 kg
* Distribution status tracking: Belum Diambil and Sudah Diambil

QR Code System

* Unique QR code generated for each user role
* Used as proof for meat collection
* QR codes can be downloaded by users

Financial Management

* Record income and expenses
* Track balance
* View transaction history

## Tech Stack

Backend: PHP (Native)
Database: MySQL
Frontend: HTML, CSS, Bootstrap
Other: QR Code generation library

## Database Setup

This project requires a database import before it can run.

Steps:

1. Open phpMyAdmin or any MySQL client
2. Create a new database named db_qurban
3. Import the SQL file provided in the project folder
4. Ensure the database configuration in koneksi.php matches your local setup

Example configuration:
$host = "localhost";
$user = "root";
$password = "1234";
$database = "db_qurban";

## How to Run

1. Place the project folder inside your web server directory
   XAMPP: htdocs
   Laragon: www

2. Start Apache and MySQL

3. Open your browser and go to
   [http://localhost/your-project-folder](http://localhost/your-project-folder)

4. Login using existing data from the database or register using an existing NIK

## Authentication System

Users log in using NIK and password. Registration is based on existing citizen data that has already been inserted into the database.

## System Workflow

1. Admin inputs citizen data
2. System automatically assigns the "warga" role
3. Admin assigns additional roles such as panitia or berqurban
4. System automatically allocates meat and generates QR codes
5. Users log in and view their QR codes
6. Panitia verifies and updates the meat collection status
7. Admin manages financial transactions

## Notes

This system uses database triggers to automate role assignment and meat distribution. QR codes function as tokens for manual verification during meat collection. The database must be imported before running the system.

## Author

Abdan Nawwaf El Hibban, M. Hisyam Al Firdaus