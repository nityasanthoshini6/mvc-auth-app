# MVC Auth & Todo API

A RESTful backend API built with Node.js, Express, and MongoDB using the **MVC (Model-View-Controller)** architecture. It features user registration, login with JWT authentication, and protected Todo CRUD routes.

## Tech Stack
* **Runtime:** Node.js (ES Modules)
* **Framework:** Express.js
* **Database:** MongoDB & Mongoose
* **Authentication:** JSON Web Tokens (JWT) & bcrypt

## Setup & Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com
   cd mvc-auth-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   Create a `.env` file in the root directory and add:
   ```env
   PORT=9000
   MONGO_URI=mongodb://127.0.0.1:27017
   DB_NAME=mvc-auth-app
   JWT_SECRET=your_secret_key
   ```

4. **Start the server**
   ```bash
   npm start
   ```

## API Endpoints

* `GET /` — Health check route.
* `POST /api/v1/users/register` — Register a new user.
* `POST /api/v1/users/login` — Log in and receive a JWT Bearer token.
* `GET /api/v1/todos` — Get all todos *(Requires Bearer Token)*.
* `POST /api/v1/todos` — Create a new todo *(Requires Bearer Token)*.
* `PUT /api/v1/todos/:id` — Update a todo by ID *(Requires Bearer Token)*.
* `DELETE /api/v1/todos/:id` — Delete a todo by ID *(Requires Bearer Token)*.
