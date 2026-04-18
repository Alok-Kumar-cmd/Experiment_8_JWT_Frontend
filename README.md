# 🧪 Experiment 8: Frontend Integration with JWT APIs (Session-Based UI)

## 📌 Objective

To build a React-based frontend that integrates with JWT authentication APIs, implements session-based authentication, and restricts access to protected routes.

---

## 🛠️ Technologies Used

* ⚛️ React (Frontend Framework)
* 🎨 Bootstrap (Styling)
* 🧩 Material UI (UI Components)
* 🔗 Axios (API Calls)
* 🖥️ Node.js + Express (Backend)
* 🔐 JSON Web Token (JWT)

---

## 📂 Project Structure

```
Experiment_8/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Login.js
│   │   │   └── Dashboard.js
│   │   ├── App.js
│   │   └── index.js
│
├── backend/
│   ├── server.js
│   └── package.json
│
└── README.md
```

---

## 🚀 Features Implemented

### 🔐 1. Login Page

* User enters username and password
* Sends request to `POST /login`
* On success:

  * JWT token is received
  * Token stored in `sessionStorage`
  * Redirects to dashboard

---

### 📊 2. Protected Dashboard

* Accessible only if token exists
* Calls `GET /protected` API
* Sends token in header:

```
Authorization: Bearer <token>
```

* Displays protected data

---

### 🚪 3. Logout Functionality

* Clears session storage:

```
sessionStorage.removeItem("token");
```

* Redirects user to login page

---

## 🔐 Authentication Flow

1. User logs in with credentials
2. Backend verifies and returns JWT token
3. Token stored in `sessionStorage`
4. Frontend sends token with API requests
5. Backend validates token before responding
6. Logout removes token and ends session

---

## ▶️ How to Run the Project

### 🔧 Backend Setup

```
cd backend
npm install
node server.js
```

Backend runs on:

```
http://localhost:5000
```

---

### 💻 Frontend Setup

```
cd frontend
npm install
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

## 🔑 Test Credentials

```
Username: admin
Password: 1234
```

---

## 📸 Screenshots

### 1️⃣ Login Page

User enters credentials

### 2️⃣ Token Stored

SessionStorage showing JWT token

### 3️⃣ Dashboard Access

Protected data displayed after clicking "Fetch Data"

### 4️⃣ Unauthorized Access

Redirect to login when token is removed

### 5️⃣ Logout

User redirected to login after logout

---

## ⚠️ Important Notes

* JWT is stored in `sessionStorage` (not localStorage)
* Protected routes are restricted based on token presence
* Authorization header is required for API access

---

## 🎯 Learning Outcomes

* Understanding of JWT authentication
* Frontend-backend API integration
* Session-based authentication handling
* Protected route implementation in React

---

## 📌 Conclusion

This experiment demonstrates how a frontend application securely interacts with backend APIs using JWT authentication and session-based access control.

---

## 👨‍💻 Author

Alok Kumar
B.Tech Student | AI/ML Enthusiast

---
