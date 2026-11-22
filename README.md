# 👥 Employee Management System — Frontend

> A fully responsive React frontend for the Employee Management System, featuring JWT-based authentication, role-based access, department-wise filtering, live dashboard stats and a Recharts bar chart.

---

## 🔗 Project Links

| Layer | Repository |
|-------|------------|
| 🎨 Frontend | [Employee_Management_Frontend](https://github.com/vijaykumar-dev28/Employee_Management_Frontend) |
| ⚙️ Backend | [Employee_Management_Backend](https://github.com/vijaykumar-dev28/Employee_Management_Backend) |

---

## 📸 Screenshots

### 🔐 Login Page
![Login](./screenshots/login.png)

### 📊 Dashboard
![Dashboard](./screenshots/dashboard_1.png)
![Dashboard Chart](./screenshots/dashboard_2.png)

### 👨‍💼 Employees Table
![Employees](./screenshots/employees.png)

### ➕ Add Employee
![Add Employee](./screenshots/add-employee.png)

### ✏️ Edit Employee
![Edit Employee](./screenshots/edit-employee.png)

---

## ⚙️ Tech Stack

| Category | Technology |
|----------|------------|
| Framework | React 19.3.1 + Vite 8.3.7 |
| Routing | react-router-dom 7.18.5 |
| HTTP Client | Axios 1.21.0 |
| Charts | Recharts 3.10.1 |
| Notifications | react-toastify 11.2.0 |
| Styling | CSS (custom) |
| Auth | JWT (stored in localStorage) |

---

## ✨ Features

- 🔐 **JWT Authentication** — Secure login with token stored in localStorage; protected routes redirect unauthenticated users
- 📊 **Live Dashboard** — Stat cards showing Total Employees, Total Departments and Active Employees; Recharts bar chart of employees per department
- 👨‍💼 **Employee Table** — List with department-wise filter dropdown and case-insensitive name search
- ➕ **Add Employee** — Form with name, email, department dropdown and salary fields with validation
- ✏️ **Edit Employee** — Pre-filled form that loads existing employee data for seamless editing
- 🗑️ **Soft Delete** — Delete action removes employee from view without permanent data loss (handled by backend)
- 🔔 **Toast Notifications** — Success and error toasts on every CRUD action using react-toastify
- 🚪 **Logout** — Clears JWT token and redirects to login

---

## 🗂️ Project Structure

```
employee-frontend/
├── screenshots/              # App screenshots for README
├── public/
├── src/
│   ├── api/
│   │   └── api.js            # Axios instance with JWT interceptor
│   ├── assets/               # Icons and images
│   │   ├── company_logo.png
│   │   ├── EmployeeLogo.png
│   │   ├── active_employees.png
│   │   ├── total_employees.png
│   │   └── total_departments.png
│   ├── components/
│   │   ├── Layout.jsx
│   │   ├── Navbar.jsx
│   │   ├── Sidebar.jsx
│   │   └── ProductRoute.jsx  # Protected route wrapper
│   ├── pages/
│   │   ├── Login.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Employees.jsx
│   │   ├── AddEmployee.jsx
│   │   └── EditEmployee.jsx
│   ├── services/
│   ├── App.jsx
│   ├── App.css
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- Backend running at `http://localhost:8080` (see [Backend Repo](https://github.com/vijaykumar-dev28/Employee_Management_Backend))

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/vijaykumar-dev28/Employee_Management_Frontend.git

# 2. Navigate into the project
cd Employee_Management_Frontend

# 3. Install dependencies
npm install

# 4. Start the development server
npm run dev
```

The app will run at **http://localhost:5173**

---

## 🔧 Environment / API Config

The Axios base URL is configured in `src/api/api.js`:

```js
const api = axios.create({
  baseURL: 'http://localhost:8080',
});
```

The JWT token is automatically attached to every request via an Axios request interceptor. Update the `baseURL` if your backend runs on a different port or is deployed.

---

## 🔐 Default Login Credentials

| Field | Value |
|-------|-------|
| Username | `admin` |
| Password | configured via environment variable in backend |

> ⚠️ The password is set through environment variables in the backend. Check your backend `.env` file or `application.properties` for the configured value.

---

## 📡 API Endpoints Used

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/login` | Login and receive JWT token |
| GET | `/employee` | Get all employees |
| GET | `/employee/{id}` | Get employee by ID |
| POST | `/employee` | Add new employee |
| PUT | `/employee/{id}` | Update employee |
| DELETE | `/employee/{id}` | Soft delete employee |
| GET | `/employee/search?name={name}` | Search employee by name |
| GET | `/department` | Get all departments |

---

## 🤝 Related Backend

This frontend connects to the **Employee Management Backend** built with:
- Spring Boot 4.0.8 + Spring Security + JWT (jjwt 0.12.6)
- Java 17 + Maven
- MySQL + JPA/Hibernate + Lombok
- BCrypt password hashing
- Soft delete with `isDeleted` flag
- Global Exception Handling
- Swagger UI (springdoc-openapi 3.1.1)

👉 [Employee_Management_Backend](https://github.com/vijaykumar-dev28/Employee_Management_Backend)

---

## 👨‍💻 Author

**Vijaykumar M**  
Java Full Stack Developer  
📧 vijaykumar.dev28@gmail.com  
🔗 [GitHub](https://github.com/vijaykumar-dev28) | [LinkedIn](https://linkedin.com/in/your-profile)
