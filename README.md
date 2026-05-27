<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4facfe,100:00f2fe&height=200&section=header&text=MediBook&fontSize=70&fontAlignY=35&desc=Doctor-Patient%20Appointment%20System&descAlignY=55&fontColor=ffffff" />

# 🏥 MediBook — Smart Healthcare Appointment Platform

> *Connecting patients with the right doctors, at the right time.*

![Made with Love](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-red?style=for-the-badge)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

<br/>

[🌐 Live Demo](https://medibook-appointment.netlify.app/) &nbsp;•&nbsp; [📖 API Docs](#-api-endpoints) &nbsp;•&nbsp; [🚀 Quick Start](#-getting-started) &nbsp;•&nbsp; [🤝 Contribute](#-contributing)

<br/>

</div>

---

## 👩‍💻 About This Project

**MediBook** is a full-stack healthcare appointment system I built to simulate a real-world doctor-patient booking workflow. It features **role-based access control** so each user type — Admin, Doctor, and Patient — gets a tailored experience, secured by JWT authentication and backed by MongoDB Atlas.

The goal was to build something that reflects production-ready architecture: clean API separation, protected routes, and a responsive UI that feels intuitive regardless of the device.

---

## ✨ What MediBook Can Do

<table>
<tr>
<td>

**👤 For Patients**
- Register and log in securely
- Browse available doctors
- Book, view, and cancel appointments
- Access a personalized dashboard

</td>
<td>

**🩺 For Doctors**
- Manage availability and schedules
- View upcoming appointments
- Update appointment statuses
- Track patient requests

</td>
<td>

**🛠️ For Admins**
- Full system control panel
- Manage all users and roles
- Monitor all appointments
- Maintain platform integrity

</td>
</tr>
</table>

---

## 🏗️ System Architecture

```
╔══════════════════════════════════════════════════╗
║         🌐 React Frontend  (Netlify)              ║
║    Components → Pages → Context → App.js         ║
╚════════════════════╤═════════════════════════════╝
                     │  HTTP Requests (REST)
                     ▼
╔══════════════════════════════════════════════════╗
║      ⚙️  Express.js REST API  (Node.js)           ║
║    Routes → Controllers → Business Logic         ║
╚════════════════════╤═════════════════════════════╝
                     │  Token Verification
                     ▼
╔══════════════════════════════════════════════════╗
║        🔐 Auth Middleware  (JWT + RBAC)           ║
║   Verify Token → Decode Role → Guard Route       ║
╚════════════════════╤═════════════════════════════╝
                     │  Database Queries
                     ▼
╔══════════════════════════════════════════════════╗
║         🍃 MongoDB Atlas  (Cloud DB)              ║
║       Users · Appointments · Schedules           ║
╚══════════════════════════════════════════════════╝
```

**Flow Summary:**
- React sends HTTP requests → Express processes them via Routes & Controllers
- Every protected route passes through JWT middleware for token validation
- RBAC enforces what each role (Admin / Doctor / Patient) can access or modify
- All data persists in MongoDB Atlas — horizontally scalable and cloud-hosted

---

## 📸 Screenshots

| View | Preview |
|------|---------|
| 🏠 **Home Page** | <img width="1919" height="968" alt="Home Page" src="https://github.com/user-attachments/assets/8a83b6c4-accf-4e6d-82b5-a37e41bac1a5" /> |
| 🔑 **Login Page** | <img width="1865" height="968" alt="Login Page" src="https://github.com/user-attachments/assets/cf9089fc-a3ef-4b0c-88ae-7f09c72a3d1d" /> |
| 👤 **Patient Dashboard** | <img width="1850" height="968" alt="Patient Dashboard" src="https://github.com/user-attachments/assets/8871f958-d42d-46c8-bd5c-86111a2716ea" /> |
| 👨‍⚕️ **Doctor Dashboard** | <img width="1858" height="965" alt="Doctor Dashboard" src="https://github.com/user-attachments/assets/54df63f3-af08-4d33-93f3-d3743b0b3c61" /> |
| 🛠️ **Admin Dashboard** | <img width="1918" height="976" alt="Admin Dashboard" src="https://github.com/user-attachments/assets/5ccda8f2-fdf2-461b-ab2e-66763bc8d82e" /> |

---

## 🗂️ Project Structure

```
MediBook/
│
├── 📁 frontend/
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # Route-level page views
│   │   ├── context/          # Auth & global state (Context API)
│   │   └── App.js            # Root component & routing
│   └── package.json
│
├── 📁 backend/
│   ├── models/               # Mongoose schemas (User, Appointment)
│   ├── routes/               # Express route definitions
│   ├── controllers/          # Core business logic
│   ├── middleware/           # JWT auth & role guards
│   └── server.js             # Entry point
│
├── 📁 config/                # Environment & DB config
├── .env.example              # Sample environment variables
└── README.md
```

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React.js | Dynamic, component-driven UI |
| **Backend** | Node.js + Express.js | RESTful API & request routing |
| **Database** | MongoDB Atlas | Cloud-hosted NoSQL storage |
| **Authentication** | JWT (JSON Web Tokens) | Stateless, secure session management |
| **Authorization** | RBAC | Role-based route protection |
| **Deployment** | Netlify + Render | Frontend & backend hosting |

---

## 🚀 Getting Started

### Prerequisites

- Node.js **v16+**
- A free [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account
- npm or yarn

### 1. Clone the Repository

```bash
git clone https://github.com/Ankita-Kumari0309/Medibook_Appointment-System.git
cd Medibook_Appointment-System
```

### 2. Install Dependencies

```bash
# Backend
cd backend && npm install

# Frontend
cd ../frontend && npm install
```

### 3. Set Up Environment Variables

Create a `.env` file inside `/backend`:

```env
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_uri
JWT_SECRET=your_super_secret_key
```

### 4. Run the App

```bash
# Start backend (from /backend)
npm run dev

# Start frontend (from /frontend)
npm start
```

> The frontend runs on `http://localhost:3000` and the backend on `http://localhost:5000`.

---

## 🔌 API Endpoints

### 🔐 Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/register` | Create a new user account |
| `POST` | `/api/auth/login` | Login and receive JWT token |

### 📅 Appointments

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/appointments` | Fetch all appointments |
| `POST` | `/api/appointments` | Book a new appointment |
| `PUT` | `/api/appointments/:id` | Update an appointment |
| `DELETE` | `/api/appointments/:id` | Cancel an appointment |

> All appointment routes are **protected** — valid JWT required in the `Authorization` header.

---

## 🌟 Key Highlights

- 🔒 **Secure by design** — JWT authentication on every protected route
- 🎭 **Three distinct roles** — Admin, Doctor, and Patient with isolated dashboards
- 🧩 **Modular architecture** — Each layer is independently testable
- ☁️ **Cloud-ready** — Deployed on Netlify (frontend) and Render (backend)
- 📱 **Fully responsive** — Works seamlessly on mobile, tablet, and desktop
- 🏥 **Real-world workflow** — Mirrors actual healthcare appointment processes

---

## 🤝 Contributing

Contributions make open source amazing! Here's how you can help:

```bash
# 1. Fork the project
# 2. Create your feature branch
git checkout -b feature/AmazingFeature

# 3. Commit your changes
git commit -m "feat: add AmazingFeature"

# 4. Push to the branch
git push origin feature/AmazingFeature

# 5. Open a Pull Request
```

Please open an **issue** first to discuss major changes. All PRs are welcome! 💙

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for details.

---

<div align="center">

## 👩‍💻 Developer

**Ankita Kumari**

[![GitHub](https://img.shields.io/badge/GitHub-Ankita--Kumari0309-181717?style=for-the-badge&logo=github)](https://github.com/Ankita-Kumari0309)

---

*If MediBook helped you or you liked the project, please consider giving it a ⭐ — it means a lot!*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4facfe,100:00f2fe&height=120&section=footer" />

</div>
