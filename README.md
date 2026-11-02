# Simple CRUD API - Node.js, Express & MongoDB

A simple backend REST API built with **Node.js**, **Express**, and **MongoDB** (Mongoose). This project demonstrates basic CRUD (Create, Read, Update, Delete) operations on a Product resource.

Based on the freeCodeCamp tutorial: [Intro to Backend Web Development](https://www.youtube.com/watch?v=KOutPbKc9UM&t=2s)

## Tech Stack

- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling (ODM)
- **Nodemon** - Auto-restart development server
- **dotenv** - Environment variable management

## Project Structure

```
web/
├── models/
│   └── product.model.js      # Mongoose schema & model for Product
├── controllers/
│   └── product.controller.js  # Business logic for CRUD operations
├── routes/
│   └── product.route.js       # API route definitions
├── .env                       # Environment variables (not committed)
├── .gitignore
├── index.js                   # Entry point - server setup & DB connection
├── package.json
└── README.md
```

## Getting Started

### Prerequisites
- Node.js installed
- MongoDB Atlas account (or a local MongoDB instance)

### Installation

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd web
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory:
   ```env
   MONGO_URI=mongodb+srv://<username>:<password>@<cluster-url>/<database-name>?retryWrites=true&w=majority
   PORT=3000
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## API Endpoints

| Method | Endpoint              | Description          |
|--------|-----------------------|----------------------|
| GET    | `/api/products`       | Get all products     |
| GET    | `/api/products/:id`   | Get a single product |
| POST   | `/api/products`       | Create a new product |
| PUT    | `/api/products/:id`   | Update a product     |
| DELETE | `/api/products/:id`   | Delete a product     |

### Example Request Body (POST / PUT)
```json
{
  "name": "Laptop",
  "quantity": 10,
  "price": 1200,
  "image": "https://example.com/laptop.jpg"
}
```

## Testing with Postman

1. Open Postman desktop app
2. Use `http://localhost:3000/api/products` as the base URL
3. Test each endpoint with the appropriate HTTP method
4. For POST and PUT requests, set the body to **raw JSON**
