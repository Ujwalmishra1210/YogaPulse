# YogaPulse 🧘

A full-stack role-based yoga management platform built with the MERN stack, connecting students with instructors and simplifying course management for yoga centers.

---

## 📸 Screenshots


<img width="1913" height="941" alt="YogaPulse_Auth" src="https://github.com/user-attachments/assets/dc20aad9-01a9-44d7-aed3-0d5675f72e82" />
<img width="1910" height="920" alt="YogaPulse" src="https://github.com/user-attachments/assets/98bc6599-e8fe-4013-a34d-1e2c9d9b2f6a" />


---

## ✨ Features

### 👨‍🎓 Student<img width="1913" height="941" alt="YogaPulse_Auth" src="https://github.com/user-attachments/assets/3af64e0c-cdc8-428e-a1d0-bd49da8047c7" />

- Browse and enroll in approved yoga classes
- Add classes to cart and complete payments via Stripe
- View enrolled classes and payment history
- Apply to become an instructor

### 👩‍🏫 Instructor
- Create, update, and manage yoga classes
- Track enrollment counts and available seats
- View class approval status from admin

### 🛡️ Admin
- Approve or reject instructor-submitted classes
- Manage all users (view, update role, delete)
- View platform-wide stats: total classes, enrollments, instructors

### 🔐 Auth & Security
- Firebase-based login and registration
- JWT authentication for protected API routes
- Role-based route protection (student / instructor / admin)

---

## 🛠️ Tech Stack

**Frontend**
- React 18, Vite
- Tailwind CSS, MUI, Framer Motion
- React Router v6, React Query
- Firebase Auth
- Stripe.js

**Backend**
- Node.js, Express.js
- MongoDB Atlas, Mongoose
- JSON Web Tokens (JWT)
- Stripe API

---

## 📁 Project Structure
```
YogaPulse/
├── frontend/        # React + Vite client
│   └── src/
│       ├── pages/   # Dashboard, Home, Classes, etc.
│       ├── config/  # Firebase config
│       └── ...
├── backend/         # Express REST API
│   └── index.js     # All routes and MongoDB logic
└── README.md
```

---

## ⚙️ Local Setup

### Prerequisites
- Node.js v18+
- MongoDB Atlas account
- Firebase project
- Stripe account (optional)

### Backend
```bash
cd backend
npm install
```

Create a `.env` file in `/backend`:
```env
PORT=5000
DB_USER=your_mongodb_username
DB_PASS=your_mongodb_password
ACCESS_SECRET=your_jwt_secret
PAYMENT_SECRET=sk_test_your_stripe_secret
```
```bash
npm start
```

### Frontend
```bash
cd frontend
npm install
```

Create a `.env` file in `/frontend`:
```env
VITE_IMG_TOKEN=your_imgbb_api_key
VITE_STRIPE=pk_test_your_stripe_publishable_key
VITE_API=http://localhost:5000
```
```bash
npm run dev
```

App runs at **http://localhost:5173**

---

## 🔑 User Roles

| Role | Access |
|------|--------|
| Student | Browse classes, enroll, make payments |
| Instructor | Create & manage classes, track enrollments |
| Admin | Full platform control, user & class management |

---

