###Learning Managment System
Step 1: Project Setup
Create a new directory for your project and navigate into it.
mkdir learning-management-app
cd learning-management-app
Initialize a new Node.js project.
npm init -y
Install necessary dependencies.
npm install express mysql ejs bcryptjs express-session express-validator
Step 2: Set up the Backend
Create a server.js file in your project directory.
Create a MySQL database named learning_management
Create users table
-- Create users table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) UNIQUE,
    password VARCHAR(255),
    email VARCHAR(255) UNIQUE,
    full_name VARCHAR(255)
);
Create courses table
-- Create courses table
CREATE TABLE courses (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255)
);

-- Insert sample data into courses table
INSERT INTO courses (name) VALUES
('Introduction to HTML'),
('CSS Fundamentals'),
('JavaScript Basics');
Create leaderboard table
-- Create leaderboard table
CREATE TABLE leaderboard (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255),
    score INT
);

-- Insert sample data into leaderboard table
INSERT INTO leaderboard (name, score) VALUES
('John Doe', 100),
('Jane Smith', 90),
('Michael Brown', 85),
('Emily Jones', 80);
Run the server.
node server.js
Step 3: Frontend Setup
Create an index.html file for the frontend.
Create a course-content.html file for the course content.
Create a leader-board.html file for the leader board.
Create a style.css file to style your HTML.
Create a script.js file to handle frontend interactions.
Step 4: Testing
Open your web browser and navigate to http://localhost:3000.