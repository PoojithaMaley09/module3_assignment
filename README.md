# 📘 Module 3 Assignment – LMS Backend with MongoDB Integration

---

##  Objective

The goal of this assignment is to integrate MongoDB into an Express.js backend using Mongoose. The system enables persistent storage of user data and includes endpoints to register users, retrieve user data by ID, and list all users.

---

##  Folder Structure

Module3_Assignment/
├── src/
│   ├── models/
│   │   └── user.model.ts
│   ├── routes/
│   │   └── userRoutes.ts
│   └── server.ts
├── .env
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
```
```
##  Tech Stack

- Node.js
- Express.js
- TypeScript
- MongoDB (via Mongoose)
- bcrypt (for password hashing)
- dotenv (for environment configuration)
- Postman (for testing APIs)

---

##  Getting Started

### 1. Clone the Repository

```
cd Module3_Assignment
```

### 2. Install Dependencies

```
npm install <what ever dependecies you want to install you can install>
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/<dbname>?retryWrites=true&w=majority
```
>  Replace `<username>`, `<password>`, and `<dbname>` with your actual MongoDB Atlas details.

### 4. Run the Server

```
npx ts-node src/server.ts
```

If successful, you should see:

```
 MongoDB connected successfully
 Server is running on http://localhost:5000
```

---

##  API Endpoints

###  POST `/api/register`

Registers a new user.

**Request Body:**

```json
{
  "name": "Poojitha",
  "email": "poojitha@gmail.com",
  "password": "securepass123"
}
```

---

###  GET `/api/user/:id`

Returns a single user (excluding password) by ID.

---

###  GET `/api/users`

Returns all registered users (excluding passwords).

---

##  Testing with Postman

You can test the API using Postman or the Postman extension in VS Code:

1. **Register User**  
   Method: `POST`  
   URL: `http://localhost:5000/api/register`  
   Body: Raw JSON with name, email, password.

2. **Get All Users**  
   Method: `GET`  
   URL: `http://localhost:5000/api/users`

3. **Get User by ID**  
   Method: `GET`  
   URL: `http://localhost:5000/api/user/<user-id>`

##  .gitignore (Important Entries)

```
node_modules/
.env
dist/
```





