# CS For Beginners 🚀

CS For Beginners is a web application designed to help beginners learn programming languages and core computer science concepts.  
The platform provides user authentication, course browsing, and course request functionality with a simple and intuitive interface.

---

## 📌 Features

- User registration and login (authentication system)
- Browse available programming courses
- Request new courses
- Beginner-friendly UI
- Responsive design using HTML, CSS, and JavaScript
- Email notifications using Nodemailer
- MongoDB database integration

---

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** Node.js, Express.js  
- **Database:** MongoDB (Mongoose)  
- **Authentication:** JWT  
- **Email Service:** Nodemailer  
- **Package Manager:** npm  

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- MongoDB (Local installation or MongoDB Atlas)
- npm

---

### 📥 Installation

1. **Clone the repository**
```bash
git clone https://github.com/ArnavRD1/CS-For-Beginners.git
cd CS-For-Beginners
```

2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Set up environment variables**

**Create a .env file in the root directory and add the following:**
```bash
EMAIL=your_email_here
PASSWORD=your_email_app_password_here
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

4. **Start the server**
```bash
   node serverFinal.js
```

5. **Open in browser**
```bash
   http://localhost:3013
```

---

🗄️ ##Database Schema

**The application uses MongoDB with Mongoose.**
**Main user schema:**

```bash
const userSchema = new mongoose.Schema({
  username: {
    type: String,
    required: true,
  },
  email: {
    type: String,
    required: true,
    unique: true,
  },
  password: {
    type: String,
    required: true,
  },
  requestedCourses: {
    type: [String],
    default: [],
  },
}, { timestamps: true });
```
**username: User display name**

**email: User email (unique)**

**password: Hashed password**

**requestedCourses: Courses requested by the user**

**timestamps: Automatically adds createdAt and updatedAt**

---

## Project Structure
```bash
.
├── css/                # Stylesheets
├── img/                # Images and icons
├── js/                 # JavaScript files (if any)
├── serverfinal.js      # Main backend server file
├── package.json
├── .env.example
├── .gitignore
├── README.md
└── ... (HTML files)

```
---

## Environment Variables
The following environment variables are required (see .env.example):

EMAIL: Email address for sending notifications
PASSWORD: App password for the email account
MONGODB_URI: MongoDB connection string

---

## Author

**Arnav RD**


