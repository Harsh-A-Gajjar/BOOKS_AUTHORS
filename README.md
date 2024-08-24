

# Book and Author Data Import Application

This project is a web-based application developed using Flask to upload, review, and save book and author data from Excel files to a SQLite database.

## Project Overview

The application allows users to:

- Upload Excel files containing book and author information.
- Review the uploaded data before confirming the import.
- Save the reviewed data into a SQLite database for storage and further use.

## Features

- **Excel File Upload**: Users can upload `.xls` or `.xlsx` files containing book and author details.
- **Data Review**: After uploading, users can view and confirm the data before saving it to the database.
- **SQLite Integration**: Data is stored in a SQLite database, making it easy to manage and retrieve information.

## Workflow and Code Architecture

The project is structured into several components:

1. **Flask Setup**: The core of the application is built using Flask, a lightweight web framework for Python.
2. **Templates**: HTML templates (`index.html` and `review.html`) are used for the user interface, allowing for file uploads and data review.
3. **File Handling**: Uploaded files are saved to a designated directory, and Pandas is used to read and process Excel files.
4. **Database Integration**: The application connects to a SQLite database where processed data is stored. The database schema includes tables for authors and books.
5. **Error Handling**: Flash messages are used to provide feedback to users about the success or failure of their actions.

## Code Architecture

- **`app.py`**: The main application file that contains all the routes and logic for file uploads, data processing, and database operations.
- **`templates/`**: A directory containing HTML files (`index.html` for file upload and `review.html` for data review).
- **`uploads/`**: A folder where uploaded Excel files are temporarily stored.
- **`schema.sql`**: SQL file that defines the schema for the SQLite database.

## How to Run

To set up and run the application locally, follow these steps:

### Set Up Your Development Environment

1. Install Python and pip if not already installed.
2. Install Flask and required libraries using pip:

   ```bash
   pip install Flask pandas openpyxl
Initialize Your Project
Create a new directory for your project and navigate into it.
Initialize a new Flask application in app.py.
Prepare the SQLite Database
Create a schema.sql file to define the tables for storing book and author information.

Initialize the database by running the setup script in Python:

  ```bash
  python -c 'from app import init_db; init_db()'
```
Run the Application
Start the Flask development server:


```python app.py```
Open your web browser and navigate to http://127.0.0.1:5000/ to access the application.

Upload and Review Data
Use the web interface to upload an Excel file.
Review the data and confirm to save it to the database.
