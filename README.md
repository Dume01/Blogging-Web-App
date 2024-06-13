# Blog Application

This is a full-stack web application built with Node.js and Express.js that allows users to create, read, update, and delete blog posts. The application consists of two main components: an internal API and a backend server.

## Components

### 1. Internal API (`index.js`)

The internal API is responsible for handling CRUD operations on blog posts. It provides the following routes:

- `GET /posts`: Retrieves a list of all posts.
- `GET /posts/:id`: Retrieves a specific post by its ID.
- `POST /posts`: Creates a new post.
- `PATCH /posts/:id`: Updates a specific post by its ID (partial update).
- `DELETE /posts/:id`: Deletes a specific post by its ID.

The API uses an in-memory data store to store blog posts. Each post has the following properties:

- `id`: A unique identifier for the post.
- `title`: The title of the post.
- `content`: The content of the post.
- `author`: The author of the post.
- `date`: The date the post was created or updated.

### 2. Backend Server (`server.js`)

The backend server is responsible for rendering the user interface and communicating with the internal API. It provides the following routes:

- `GET /`: Renders the main page, displaying a list of all posts.
- `GET /new`: Renders a form for creating a new post.
- `GET /edit/:id`: Renders a form for editing an existing post.
- `POST /api/posts`: Creates a new post by sending a request to the internal API.
- `POST /api/posts/:id`: Updates an existing post by sending a request to the internal API.
- `GET /api/posts/delete/:id`: Deletes an existing post by sending a request to the internal API.

The server uses EJS (Embedded JavaScript) as the templating engine to render the views.

## Getting Started

To run the application locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/blog-application.git`
2. Navigate to the project directory: `cd blog-application`
3. Install dependencies: `npm install`
4. Start the internal API: `node index.js`
5. Start the backend server: `node server.js`
6. Open your web browser and visit `http://localhost:3000` to access the application.

## Dependencies

The following dependencies are used in this project:

- `express`: Web application framework for Node.js.
- `body-parser`: Middleware for parsing request bodies.
- `axios`: Promise-based HTTP client for making API requests.
- `ejs`: Templating engine for rendering views.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
