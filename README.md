# Bookshelf API

This project is a back-end application developed as part of the **Dicoding** course, "Belajar Membuat Aplikasi Back-End untuk Pemula dengan Google Cloud." It provides a RESTful API for managing a personal bookshelf, allowing users to add, read, update, and delete book records.

## Features

* **Add Books**: Create a new book with title, author, year, and reading status.
* **Get All Books**: Retrieve all saved books, with optional filters.
* **Get Book by ID**: Retrieve detailed information for a specific book.
* **Update Book**: Modify details of an existing book.
* **Delete Book**: Remove a book from the collection.

## Technologies Used

* **Node.js**: JavaScript runtime environment.
* **Hapi.js**: A rich framework for building powerful APIs.
* **ESLint**: Linter for maintaining code quality.
* **Google Cloud Platform** *(optional)*: For deployment and scalability.

## Prerequisites

* Node.js and npm installed.
* Google Cloud account (optional, for deployment).

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/rayhanfay/bookshelf-api.git
   cd bookshelf-api
   ```

2. **Install Dependencies**:

   ```bash
   npm install
   ```

3. **Run the Application**:

   ```bash
   npm start
   ```

   The server will start at `http://localhost:5000` by default.

## API Endpoints

* `GET /books`: Retrieve all books (with optional query filters: `name`, `reading`, `finished`).
* `GET /books/{id}`: Retrieve a specific book by its ID.
* `POST /books`: Add a new book.
* `PUT /books/{id}`: Update an existing book by ID.
* `DELETE /books/{id}`: Delete a book by ID.

## Project Structure

* `src/`: Main source code folder.
  * `handler.js`: Handles request logic.
  * `routes.js`: Defines server routes.
  * `books.js`: In-memory storage for book data.

## Deployment

To deploy this application on Google Cloud:

1. Set up a Google Cloud project.
2. Enable App Engine or Cloud Run.
3. Add `app.yaml` (for App Engine) or a `Dockerfile` (for Cloud Run).
4. Deploy using:

   ```bash
   gcloud app deploy
   # or for Cloud Run:
   gcloud run deploy
   ```
