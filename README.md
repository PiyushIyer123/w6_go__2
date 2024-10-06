
  

# Go CRUD API Example

  

This is a simple CRUD API for managing books, written in Go using the `net/http` package and `gorilla/mux` for routing. This API allows you to create, read, update, and delete books.

  

## Prerequisites

  

- Go (version 1.16 or later)

- Postman (for testing the API)

  
  

3. Install the `gorilla/mux` package.

  

```sh

go  get  -u  github.com/gorilla/mux

  

```

  

## Running the API

  

To run the API, use the following command:

  

```sh

go  run  *.go

  

```

  

You should see the following output indicating that the server is running on port 8000:

  

```

Starting server at port 8000

  

```

  

## API Endpoints

  

The following endpoints are available:

  

-  **GET**  `/books` - Retrieve all books

-  **GET**  `/books/{id}` - Retrieve a book by ID

-  **POST**  `/books` - Create a new book (send JSON body with `title` and `author`)

-  **PUT**  `/books/{id}` - Update a book by ID (send JSON body with `title` and `author`)

-  **DELETE**  `/books/{id}` - Delete a book by ID

  

## Testing the API with Postman

  

### 1. GET /books

  

-  **Request**: `GET http://localhost:8000/books`

-  **Response**:

  

JSON

  

```json

[

{

"id": "1",

"title": "2 States",

"author": "Chetan Bhagat"

},

{

"id": "2",

"title": "War and Peace",

"author": "Leo Tolstoy"

}

]

  
  

```

!GET /books

### 2. GET /books/{id}

  

-  **Request**: `GET http://localhost:8000/books/1`

-  **Response**:

  

JSON

  

```json

{

"id": "1",

"title": "2 States",

"author": "Chetan Bhagat"

}
```

  

!GET /books/{id}

  

### 3. POST /books

  

-  **Request**: `POST http://localhost:8000/books`

-  **Body**:

  

JSON

```json

{

"title": "New Book",

"author": "Shakespeare"

}
```

  
  

-  **Response**:

  

JSON

  

```json

{

"id": "123456",

"title": "New Book",

"author": "Graham Potter"

}
```

  
  

!POST /books

  

### 4. PUT /books/{id}

  

-  **Request**: `PUT http://localhost:8000/books/1`

-  **Body**:

  

JSON
```json

{

"title": "Updated Book",

"author": "Rabindranath Tagore"

}
```

  

-  **Response**:

  

JSON
```json

{

"id": "1",

"title": "Updated Book",

"author": "Rabindranath Tagore"

}
```

!PUT /books/{id}

  

### 5. DELETE /books/{id}

  

-  **Request**: `DELETE http://localhost:8000/books/1`

-  **Response**:

  

JSON

  

```json

[

{

"id": "2",

"title": "War and Peace",

"author": "Leo Tolstoy"

}

]
```

  

!DELETE /books/{id}

  

## Conclusion

  

This README file provides a detailed explanation of the Go CRUD API and steps to test it using Postman. Below are each endpoints to test the API in postman.

  
  

GET /books - Retrieve all books

GET /books/{id} - Retrieve a book by ID

POST /books - Create a new book (send JSON body with title and author)

PUT /books/{id} - Update a book by ID (send JSON body with title and author)

DELETE /books/{id} - Delete a book by ID