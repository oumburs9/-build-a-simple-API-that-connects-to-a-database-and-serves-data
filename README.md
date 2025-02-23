# -build-a-simple-API-that-connects-to-a-database-and-serves-data

You're right! Since you're running the server with `node server.js`, I’ve updated the **README.md** accordingly. Here’s the **final version**:

```md
# 🚀 User API - Endpoints Documentation

## **Base URL**
```
http://localhost:5000/api/users
```
*(Replace with your deployed URL if hosting online)*

---

## **📌 Authentication Endpoints**

### **🔹 Register a New User**
**`POST /register`**  

✅ **Request Body (JSON)**
```json
{
  "name": "John Doe",
  "email": "johndoe@example.com",
  "password": "securepassword"
}
```
✅ **Response (Success)**
```json
{
  "message": "User registered successfully!"
}
```

---

### **🔹 Login a User**
**`POST /login`**  

✅ **Request Body (JSON)**
```json
{
  "email": "johndoe@example.com",
  "password": "securepassword"
}
```
✅ **Response (Success)**
```json
{
  "token": "your-jwt-token"
}
```

---

## **📌 User Management Endpoints**

### **🔹 Get All Users**
**`GET /`**  

✅ **Headers**
```json
{
  "Authorization": "Bearer your-jwt-token"
}
```
✅ **Response (Success)**
```json
[
  {
    "id": "12345",
    "name": "John Doe",
    "email": "johndoe@example.com",
    "role": "user"
  }
]
```

---

### **🔹 Get a Specific User**
**`GET /:id`**  
✅ **Example:** `/api/users/12345`  
✅ **Response (Success)**
```json
{
  "id": "12345",
  "name": "John Doe",
  "email": "johndoe@example.com",
  "role": "user"
}
```

---

### **🔹 Update User**
**`PUT /:id`**  
✅ **Example:** `/api/users/12345`  
✅ **Request Body (JSON)**
```json
{
  "name": "Updated Name",
  "email": "updated@example.com"
}
```
✅ **Response (Success)**
```json
{
  "message": "User updated successfully!"
}
```

---

### **🔹 Delete User**
**`DELETE /:id`**  
✅ **Example:** `/api/users/12345`  
✅ **Response (Success)**
```json
{
  "message": "User deleted successfully!"
}
```

---

## **📌 Extra Features**
- 🔒 **JWT Authentication:** Secure access to protected routes.
- 🔄 **Pagination & Filtering:** Fetch users with optional query parameters.
- ⚡ **Built with Express.js & MongoDB.**

---

## **📌 How to Run the Project**
1. **Clone the repository**  
   ```sh
   https://github.com/oumburs9/-build-a-simple-API-that-connects-to-a-database-and-serves-data.git
   ```
2. **Go to the project directory**  
   ```sh
   cd user-api
   ```
3. **Install dependencies**  
   ```sh
   npm install
   ```
4. **Set up environment variables**  
   - Create a `.env` file and add:  
     ```
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_secret_key
     PORT=5000
     ```
5. **Start the server**  
   ```sh
   node server.js
   ```

--- 

You're now all set! Let me know if you need any modifications. 🚀🔥
