# Hashing_technique-For-Transmitting-Data-Securely

## A-New-Hashing-Technique
Project
# Flask File Upload and Authentication System

## Overview
This project is a simple web application built using Flask that allows users to register, log in, and upload files. Each uploaded file is stored in a user-specific directory, and its integrity is verified using a SHA-512 hash. The system uses MySQL for user authentication and file tracking.

## Features
- **User Registration**: Allows users to create an account.
- **User Login**: Authenticates users before allowing file uploads.
- **File Upload**: Enables users to upload files securely.
- **File Integrity Check**: Computes and stores a SHA-512 hash for each uploaded file.
- **Session Management**: Uses Flask sessions to manage user authentication.
- **Database Integration**: Stores user and file data in a MySQL database.

## Technologies Used
- Python (Flask framework)
- MySQL (Database)
- HTML & CSS (Frontend)
- Werkzeug (Secure filename handling)
- Hashlib (File integrity check)

## Installation and Setup
### Prerequisites
Ensure you have the following installed:
- Python 3
- MySQL Server
- Flask and required dependencies

### Step 1: Clone the Repository
```sh
$ git clone https://github.com/yourusername/flask-file-upload.git
$ cd flask-file-upload
```

### Step 2: Install Dependencies
```sh
$ pip install flask mysql-connector-python werkzeug
```

### Step 3: Configure Database
1. Create a MySQL database:
```sql
CREATE DATABASE project17;
```
2. Create necessary tables:
```sql
CREATE TABLE register (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE filesdata (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL,
    filename TEXT NOT NULL,
    hash TEXT NOT NULL
);
```

### Step 4: Run the Application
```sh
$ python app.py
```
The application will be available at `http://localhost:5000`.

## Usage
1. Register a new user on the homepage.
2. Log in using the registered credentials.
3. Navigate to the upload page and upload a file.
4. The file will be stored in `static/uploads/<username>/` and hashed for integrity.

## Directory Structure
```
flask-file-upload/
│── static/
│   └── uploads/
│── templates/
│   ├── index.html
│   ├── dashboard.html
│   ├── upload.html
│── app.py
│── README.md
```

## License
This project is licensed under the MIT License.

## Contributors
- Your Name (@yourgithubhandle)

## Contact
For questions or suggestions, please open an issue or contact [your email].

