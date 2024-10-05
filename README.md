# MERN Book Store Application

A full-stack Book Store application built using the MERN (MongoDB, Express, React, Node.js) stack. This application allows users to browse books, manage their collections, and submit queries via a contact page. It includes essential features like user authentication and CRUD operations for book management.

## Features

- **User Authentication**: Signup and login functionality for users.
- **Book Management**:
  - Add new books to the store.
  - Update existing book details.
  - Delete books from the store.
- **Book Browsing**: View a list of available books with details like title, author, and description.
- **Contact Page**: A form for users to submit queries or feedback.
  
## Installation

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/en/download/)
- [MongoDB](https://www.mongodb.com/try/download/community)

### Steps

1. Clone the repository:
   ```bash
   https://github.com/malikEhsan09/BookStore.git
   ```

2. Navigate into the project directory:
   ```bash
   cd book-store-mern
   ```

3. Install server-side dependencies:
   ```bash
   cd server
   npm install
   ```

4. Install client-side dependencies:
   ```bash
   cd ../client
   npm install
   ```

5. Set up environment variables:
   - Create a `.env` file in the `server` directory with the following values:
     ```env
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret_key
     ```

6. Run the MongoDB service on your machine:
   ```bash
   mongod
   ```

7. Start the application:
   - To start the server, run:
     ```bash
     cd server
     npm start
     ```
   - To start the client, run:
     ```bash
     cd ../client
     npm start
     ```

8. Open your browser and go to `http://localhost:3000` to access the application.

## Project Structure

- **server/**: Contains the backend code (Node.js, Express, MongoDB).
  - `models/`: Mongoose models for handling data.
  - `routes/`: API routes for authentication, book management, and contact form.
  - `controllers/`: Logic for handling API requests.
  - `middlewares/`: Middleware for authorization and other tasks.
  
- **client/**: Contains the frontend code (React).
  - `src/components/`: React components for UI (Books, Auth, Contact).
  - `src/pages/`: Pages like Home, Signup, Login, Book List, etc.
  - `src/services/`: Functions for making API requests to the backend.
  - `src/context/`: Context API for managing state (e.g., authentication, book data).
  
## Key Functionalities

### User Authentication
- **Signup**: Users can create an account using a unique email and password.
- **Login**: Users can log in to their account with their credentials.
- **JWT Token**: Authentication is handled using JSON Web Tokens (JWT) for secure session management.

### Book Management
- **Add Book**: Authenticated users can add books to the store with details like title, author, and description.
- **Update Book**: Users can edit the information of books they have added.
- **Delete Book**: Users can remove books from the store.

### Contact Page
- **Submit Queries**: Users can fill out a contact form to submit their queries or feedback, which is stored in the backend.

## API Endpoints

### Authentication
- **POST** `/api/auth/signup`: Register a new user.
- **POST** `/api/auth/login`: Log in with existing user credentials.

### Books
- **GET** `/api/books`: Fetch all books.
- **POST** `/api/books`: Add a new book (authenticated).
- **PUT** `/api/books/:id`: Update a book's details (authenticated).
- **DELETE** `/api/books/:id`: Delete a book (authenticated).

### Contact
- **POST** `/api/contact`: Submit a contact form query.

## Technologies Used

- **Frontend**:
  - React.js
  - React Context API (State Management)
  - Axios (API requests)
  
- **Backend**:
  - Node.js
  - Express.js
  - MongoDB (Mongoose)
  - JWT (JSON Web Token for Authentication)

## Future Improvements

- Implement a search functionality for books.
- Add a profile page where users can manage their information and view their added books.
- Improve the UI/UX for better user interaction.
- Add pagination to the book list.

## Feedback

Feel free to provide feedback or report issues by opening a new issue on this repository.
