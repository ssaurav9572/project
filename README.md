# projecBook Library Management System

This Spring Boot application provides RESTful endpoints to manage a book library, including CRUD operations for books, authors, and book rentals.
Setup Instructions

    Clone the Repository:

    bash

git clone https://github.com/your-username/book-library-management.git
cd book-library-management

Database Configuration:

    Configure your database settings in application.properties file located in src/main/resources.

Build and Run the Application:

arduino

./mvnw spring-boot:run

Alternatively, you can build a JAR file and run it:

bash

    ./mvnw clean package
    java -jar target/book-library-management-1.0.0.jar

    Access the Application:

    Once the application is running, you can access the endpoints using a tool like Postman or cURL.

    Base URL: http://localhost:8080/api

Endpoints
Books

    GET /books: Get all books
    GET /books/{id}: Get book by ID
    POST /books: Create a new book
    PUT /books/{id}: Update book by ID
    DELETE /books/{id}: Delete book by ID

Authors

    GET /authors: Get all authors
    GET /authors/{id}: Get author by ID
    POST /authors: Create a new author
    PUT /authors/{id}: Update author by ID
    DELETE /authors/{id}: Delete author by ID

Rentals

    GET /rentals: Get all rentals
    GET /rentals/{id}: Get rental by ID
    POST /rentals: Create a new rental
    DELETE /rentals/{id}: Delete rental by ID

Additional Endpoints

    GET /books/author/{authorId}: Get books by author ID
    GET /books/available: Get books available for rent
    GET /books/rented: Get books currently rented

Sample Requests
Create Book

http

POST /api/books
Content-Type: application/json

{
    "title": "Java Programming",
    "isbn": "978-0123456789",
    "publicationYear": 2020
}

Get Book by ID

http

GET /api/books/1

Update Book

http

PUT /api/books/1
Content-Type: application/json

{
    "title": "Java Programming (Updated)",
    "isbn": "978-9876543210",
    "publicationYear": 2022
}

Delete Book

http

DELETE /api/books/1
