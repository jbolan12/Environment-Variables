# Environment-Variables

# User Authentication System with Express, Passport, and PostgreSQL

This project is an authentication system built using Express, Passport, PostgreSQL, and bcrypt for password encryption. It includes routes for user registration, login, logout, and an authenticated-only page.

## Table of Contents

- [Installation]
- [Environment Variables]
- [Usage]
- [File Structure]
- [Dependencies]
- [Features]
- [License]

## Installation

1. **Clone the repository:**

   ```bash
[   git clone (https://github.com/jbolan12/Environment-Variables)   ]


## Navigate to the project directory:

bash
cd your-repo-name

## Install dependencies:

bash
npm install

## Set up PostgreSQL Database:

->Make sure PostgreSQL is installed and running.

Create a database and a users table. For example:

sql

CREATE DATABASE your_database_name;
\c your_database_name
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL
);

## Environment Variables:

->Create a .env file in the root directory and add the following variables:

plaintext

PG_USER=your_database_user
PG_HOST=localhost
PG_DATABASE=your_database_name
PG_PASSWORD=your_database_password
PG_PORT=5432
SESSION_SECRET=your_secret_key

## Usage
Run the server:

bash
npm start

## Access the application:

Open your browser and go to http://localhost:3000.

## File Structure

bash

project-root/
├── public/               # Static files (CSS, images, etc.)
├── views/                # EJS templates for rendering views
│   ├── home.ejs
│   ├── login.ejs
│   ├── register.ejs
│   └── secrets.ejs
├── .env                  # Environment variables
├── app.js                # Main application file
└── package.json          # Project metadata and dependencies


## Dependencies
express: Web framework for Node.js
body-parser: Middleware to parse incoming request bodies
pg: PostgreSQL client for Node.js
bcrypt: Library for hashing passwords
passport: Authentication middleware for Node.js
passport-local: Local authentication strategy for Passport
express-session: Middleware for managing sessions
dotenv: Loads environment variables from .env file


## To install all dependencies, run:

bash
npm install


## Features
User Registration: Secure registration with bcrypt for password hashing.
User Login: Local authentication strategy using Passport.
Session Management: Sessions stored using express-session.
Authentication Protection: Routes restricted to authenticated users only.
Environment Configuration: Secure database credentials via .env file.


## License
This project is licensed under the MIT License.
