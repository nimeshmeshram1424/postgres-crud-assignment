# Postgres CRUD Assignment

This project demonstrates CRUD (Create, Read, Update, Delete) operations in PostgreSQL using Python (psycopg2) and also shows how to export database records into a JSON file.

## Environment Setup

1. PostgreSQL 17 installed locally.
2. pgAdmin 4 for database management.
3. Python 3.8+ installed.
4. Python libraries required:
   - `psycopg2`
   - `json` (built-in)

Install psycopg2 via pip if not already installed:

      pip install psycopg2

## Files (Structure):

1. postgres_crud.py → Python script for CRUD operations and JSON export.
2. students.json → Sample export of student data.
3. README.md → This file.

## How to Run:

1. Ensure PostgreSQL server is running and your database (Database1) exists.
2. Ensure the table student_schema.students exists in your database.
   1. Open pgAdmin 4 or use SQL shell.
   2. Create a database, schema, table and columnns
3. Update the database connection details in postgres_crud.py:
   1. dbname="Database1"
   2. user="postgres"
   3. password="your_password"
   4. host="localhost"
   5. port=5432

## Run the script:

      python postgres_crud.py

## Sample Output:

Connection successful!

🎉 Student Alice inserted successfully!

🎉 Student Bob inserted successfully!

Student Records: [(12, 'Alice', 21, 'Statistics', 'alice@example.com'), (13, 'Bob', 22, 'Computer Science', 'bob@example.com')]

Student updated successfully!

Student deleted successfully!

Data exported to students.json

## JSON Export Example:

       [
   
          {
              "student_id": 12,
              "name": "Alice",
              "age": 21,
              "department": "Statistics",
              "email": "alice@example.com"
          },
          {
              "student_id": 13,
              "name": "Bob",
              "age": 22,
              "department": "Computer Science",
              "email": "bob@example.com"
          }
      ]

## Features:

1. Connect to PostgreSQL with Python
2. Insert new student records
3. Fetch all student records
4. Update student data
5. Delete student records
6. Export database records to JSON
