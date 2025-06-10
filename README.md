# Vidtube Backend 🎥

Vidtube is the backend of a video streaming platform (similar to YouTube) built using **Node.js**, **Express.js**, and **MongoDB**. It provides secure and scalable RESTful APIs for handling user authentication, video upload, video streaming, likes, comments, and more.

---

## 🌐 Features

- ✅ User registration and login (JWT authentication)
- 🎞️ Upload and stream videos
- 👍 Like/dislike functionality
- 💬 Comment system
- 🧾 Video details (title, description, views, etc.)
- 🔒 Protected routes for authenticated users
- 📁 MongoDB integration for persistent storage

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT (JSON Web Token)
- **File Upload**: Multer or Cloudinary (depending on your setup)
- **Environment Management**: dotenv

---

## 📁 Project Structure

vidtube-backend/
│
├── controllers/ # Business logic for APIs
├── models/ # Mongoose schemas
├── routes/ # All API endpoints
├── middlewares/ # Auth and error handling
├── utils/ # Helper functions
├── config/ # DB connection and config
├── uploads/ # Video/image storage (if local)
├── .env # Environment variables
├── server.js # Entry point
└── package.json

yaml
Copy
Edit

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/vidtube-backend.git
cd vidtube-backend
2. Install dependencies
bash
Copy
Edit
npm install
3. Create a .env file
env
Copy
Edit
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
4. Run the server
bash
Copy
Edit
npm start
The server will run on http://localhost:5000.

🔐 API Authentication
Use the Authorization header with a Bearer token for protected routes:

h
Copy
Edit
Authorization: Bearer <your_token>
📬 API Endpoints Overview
Auth
POST /api/auth/register – Register new user

POST /api/auth/login – Login and get token

Videos
POST /api/videos/upload – Upload video (auth required)

GET /api/videos/ – Get all videos

GET /api/videos/:id – Get video by ID

POST /api/videos/:id/like – Like a video

POST /api/videos/:id/dislike – Dislike a video

Comments
POST /api/comments/:videoId – Add a comment

GET /api/comments/:videoId – Fetch comments for a video

🧪 Testing
Use Postman or any API testing tool to test your routes. Make sure to include the Bearer token for protected routes.
