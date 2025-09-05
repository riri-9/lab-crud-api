# lab-crud-api
# Lab CRUD API

A simple **Node.js + Express + MySQL** REST API for managing **students** and **courses**.  
This project demonstrates CRUD (Create, Read, Update, Delete) operations with a clean structure.

---

## Project Overview
This API provides:
- **Students management**: create, read, update, and delete students
- **Courses management**: create, read, update, and delete courses
- **Health check endpoint** for testing server and database connection

It uses:
- **Express.js** for building the REST API
- **MySQL2** for database connection
- **dotenv** for environment variables
- **CORS** for cross-origin requests

---

##  Setup Steps

1. **Clone the repository**
   git clone https://github.com/riri-9/lab-crud-api.git
   cd lab-crud-api|

2. **Install dependencies**
npm install

3. **Set up environment variables**
Create a .env file in the root folder:
DB_HOST=localhost
DB_USER=root
DB_PASS=
DB_NAME=lab_crud
PORT=3000

4. **Set up the MySQL database**
CREATE DATABASE lab_crud;

CREATE TABLE courses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  code VARCHAR(50) UNIQUE NOT NULL,
  title VARCHAR(255) NOT NULL,
  units INT NOT NULL
);

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  email VARCHAR(255) UNIQUE NOT NULL,
  course VARCHAR(100),
  year_level INT
);

5. **Start the server**
npm start
