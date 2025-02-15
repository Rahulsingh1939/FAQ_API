# FAQ API Backend

## 📌 Overview
This is a multilingual FAQ API built using **Node.js, Express, MongoDB, and Redis**. It supports **language-based translations** and caching for better performance.

## 🚀 Features
-  Create, Read, Update, and Delete (CRUD) FAQs
-  Multilingual support with **Google Translate API**
-  Language selection via **?lang=** query parameter
-  Caching with **Redis** for optimized performance
-  **Unit Tests** using **Mocha, Chai, and Supertest**

---

##  Folder Structure
```
backend/
│── config/        # Configuration files of Database
│── controllers/   # Business logic for API routes
│── models/        # MongoDB models
│── routes/        # Express routes
│── tests/         # Unit tests
│── utils/         # Utilities for redis and translation
│── server.js      # Main entry point
│── .env           # Environment variables
│── package.json   # Dependencies & scripts
```

---

## Tech Stack
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Caching**: Redis
- **Translation**: Google Translate API (or `googletrans` alternative)
- **Testing**: Mocha, Chai, Supertest

---

##  Installation
###  Clone the Repository
```sh
git clone https://github.com/nishujangra/faq-api.git
cd faq-api
```

###  Install Dependencies
```sh
npm install
```

### Set Up Environment Variables
Create a **.env** file in the root folder and add the following:
```env
PORT=5000
MONGO_URI="YOUR MONGO URL"
REDIS_PASSWORD=******
```

### Start the Server
```sh
npm start
```

Or, for development with **Nodemon**:
```sh
npm run dev
```

---

##  API Endpoints
###  **FAQ Endpoints**
| Method | Endpoint | Description |
|--------|---------|-------------|
| **POST** | `/api/faqs` | Create a new FAQ |
| **GET** | `/api/faqs` | Get all FAQs |
| **DELETE** | `/api/faqs/:id` | Delete an FAQ |

####  **Example: Fetch FAQs with Language Selection**
```sh
GET /api/faqs?lang=hi
```
Response:
```json
[
  {
    "question": "Node.js क्या है?",
    "answer": "Node.js एक जावास्क्रिप्ट रनटाइम है।"
  }
]
```

---
