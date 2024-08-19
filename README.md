# Book Vault - Mock JSON Server

This repository contains a mock JSON server that provides API endpoints for the "Book Vault" project. The JSON server is deployed on Render.com and simulates a backend to serve book data, making it easier to develop and test frontend applications.

## Project Overview

**Book Vault** is a web application designed to help users manage their personal book collections. The application fetches data from a mock JSON server, which provides information on various books, including titles, authors, genres, ratings, and more.

## API Endpoints

Once deployed, the JSON server will expose the following endpoints:

- **GET** `/books` - Returns a list of all books.
- **GET** `/books/:id` - Returns a specific book by its ID.
- **POST** `/books` - Adds a new book to the collection.
- **PATCH** `/books/:id` - Updates the details of a specific book.
- **DELETE** `/books/:id` - Deletes a specific book from the collection.

### Example Data Structure

The `db.json` file contains the following structure:

```json
{
  "books": [
    {
      "id": "69",
      "title": "The Lean Startup: How Today's Entrepreneurs Use Continuous Innovation to Create Radically Successful Businesses",
      "author": "Eric Ries",
      "pages": 336,
      "coverImage": "https://covers.openlibrary.org/b/id/7104760-L.jpg",
      "publicationDate": "2011-09-13",
      "genre": "Business",
      "synopsis": "A guide to building successful startups by applying lean principles, focusing on continuous innovation, validated learning, and rapid iteration.",
      "language": "English",
      "publisher": "Currency",
      "format": "Hardcover, Paperback, eBook, Audiobook",
      "edition": "",
      "rating": "5"
    },
    ...
  ]
}
```

## Getting Started

### Prerequisites

- Node.js and npm installed on your local machine.
- A Render.com account for deployment.

### Local Development

To run the mock JSON server locally:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ImeldaHope/bookvault_data.git
   cd bookvault_data
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Start the server:**

   ```bash
   npx json-server --watch books.json --port 3000
   ```

   The server will run on `http://localhost:3000`.

### Deployment on Render.com

To deploy the JSON server on Render.com:

1. **Create a new web service** on Render.com.

2. **Connect the repository** to your Render.com account.

3. **Set the start command** to:

   ```bash
   npx json-server --watch db.json --port 3000
   ```

4. **Deploy the service**.

5. Once deployed, the API endpoints will be accessible at `https://book-vault.onrender.com/books`.

## Contributing

If you'd like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the ISC License.
