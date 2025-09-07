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
| Method | Endpoint                  | Description              |
|--------|---------------------------|--------------------------|
| POST   | /api/user/register        | Register new user        |
| POST   | /api/user/login           | Login user               |
| POST   | /api/user/logout          | Logout user              |
| POST   | /api/user/forgot-password | Send password reset link |
| POST   | /api/user/reset-password/:token | Reset password      |

---

### 👥 Users
| Method | Endpoint                          | Description                  |
|--------|-----------------------------------|------------------------------|
| GET    | /api/user/                        | Admin: Get all users         |
| GET    | /api/user/clients                  | Admin: Get all clients       |
| GET    | /api/user/freelancers              | Admin: Get all freelancers   |
| GET    | /api/user/profile/:userId          | Get user profile             |
| PUT    | /api/user/changepassword           | Change password              |
| PUT    | /api/user/update-client            | Update client profile        |
| PUT    | /api/user/update-freelancer        | Update freelancer profile    |
| PUT    | /api/user/update-account-status    | Admin: Toggle account status |
| GET    | /api/user/stats/counts             | Admin: Get system counts     |
| GET    | /api/user/stats/ratio              | Admin: Client/Freelancer ratio |
| GET    | /api/user/loginStats/byMonth       | Admin: Monthly login stats   |
| GET    | /api/user/:userId                  | Admin: Get single user       |
| DELETE | /api/user/delete/:id               | Delete user account          |

---

### 💼 Jobs
| Method | Endpoint                           | Description                   |
|--------|------------------------------------|-------------------------------|
| POST   | /api/job/create                    | Create job (Client only)      |
| GET    | /api/job/                          | Get all jobs                  |
| GET    | /api/job/activated                 | Get activated jobs (public)   |
| GET    | /api/job/getJobsForClientDash      | Jobs for client dashboard     |
| GET    | /api/job/getJobsForClientPublic    | Jobs visible for client       |
| POST   | /api/job/save-job                  | Save job                      |
| POST   | /api/job/unsave-job                | Unsave job                    |
| DELETE | /api/job/delete-job/:jobId         | Delete job                    |
| PUT    | /api/job/update-job-status         | Admin: Update job status      |
| GET    | /api/job/savedJop/:userId          | Get saved jobs for user       |
| GET    | /api/job/jobs/client/:clientId     | Get jobs posted by a client   |
| GET    | /api/job/:jobId                    | Admin: Get single job         |

---

### 📑 Applications
| Method | Endpoint                                                      | Description                  |
|--------|---------------------------------------------------------------|------------------------------|
| POST   | /api/application/apply                                        | Apply for a job (upload CV) |
| GET    | /api/application/myAppliedJobs                                | Get my applied jobs          |
| DELETE | /api/application/deleteApplicationForFriendApplication/:id    | Delete friend’s application |
| DELETE | /api/application/deleteApplicationForFriendJop/:id            | Delete job-related application |

---

### 🤝 Freelancer Join Requests
| Method | Endpoint                              | Description                        |
|--------|---------------------------------------|------------------------------------|
| POST   | /api/work/applyToWork                 | Apply to join (CV + Profile Picture) |
| GET    | /api/work/approved-freelancers        | Get approved freelancers            |
| GET    | /api/work/pending-freelancers         | Admin: Get pending requests         |
| DELETE | /api/work/delete-join/:id             | Delete join request                 |
| POST   | /api/work/add/csv                     | Upload freelancers via CSV          |
| GET    | /api/work/export-csv                  | Admin: Export freelancers as CSV    |
| GET    | /api/work/download/freelancers.csv    | Download freelancers CSV file       |
| GET    | /api/work/singleJoinRequest/:id       | Admin: Get single join request      |
| PUT    | /api/work/update-work-status          | Admin: Update freelancer status     |
| PUT    | /api/work/updateJoinRequest/:id       | Admin: Update join request details  |

---

### 📩 Contact
| Method | Endpoint     | Description            |
|--------|--------------|------------------------|
| POST   | /api/contact | Send contact message   |

---


## 🚀 Getting Started

### 📁 Clone the repository

```bash
git clone https://github.com/AngeloEsam/ERSHAD-Node.git
cd ERSHAD-Node
--

##  Run the Server
npm install
npm start
