# Ershad Backend

This is the **backend API** for the Ershad platform, built with **Node.js, Express, and MongoDB**.  
It handles authentication, job postings, applications, freelancer management, and more.  

---

## 🚀 Features

- 🔐 **Authentication & Authorization**
- 👥 **User Management** (Clients, Freelancers, Admins)
- 💼 **Job Management**
- 📑 **Applications**
- 🤝 **Freelancer Join Requests**
- 📩 **Contact Messages**
- 📊 **Admin Dashboard Statistics**
- 📂 **File Uploads** (CVs, Profile Pictures, Company Logos)
- 📦 **Export Data to CSV**

---

## 🛠️ Tech Stack

- **Backend Framework:** Node.js (Express)
- **Database:** MongoDB (Mongoose)
- **Authentication:** JWT + Cookies
- **File Uploads:** Multer
- **Security:** bcrypt, validator
- **Other Tools:** dotenv, cors, nodemailer, csv-writer

---

## 🛠️ API Endpoints

### 🔐 Authentication
| Method | Endpoint              | Description   |
|--------|-----------------------|---------------|
| POST   | /api/auth/register    | Register user |
| POST   | /api/auth/login       | Login user    |

---

### 📂 Projects & Partners
| Method | Endpoint        | Description       |
|--------|----------------|-------------------|
| GET    | /api/projects  | Get projects      |
| POST   | /api/projects  | Create project    |
| GET    | /api/partners  | Get partners      |
| POST   | /api/partners  | Add partner       |

---

### 📑 Contracts & Work
| Method | Endpoint              | Description        |
|--------|-----------------------|--------------------|
| POST   | /api/contracts        | Create contract    |
| GET    | /api/work             | Get work items     |
| POST   | /api/addition         | Add addition       |
| POST   | /api/deduction        | Add deduction      |
| POST   | /api/workConfirmation | Confirm work       |

---

### 🏗️ Materials & Products
| Method | Endpoint        | Description        |
|--------|----------------|--------------------|
| GET    | /api/materials  | Get materials      |
| GET    | /api/categories | Get categories     |
| GET    | /api/products  | Get products       |



## 🚀 Getting Started

### 📁 Clone the repository

```bash
git clone https://github.com/your-username/ershad-backend.git
cd ershad-backend
--

##  Run the app
npm install
npm start
