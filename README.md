# Exceleron - AI-Powered Excel Analytics & Visualization Platform

![Project Banner](https://via.placeholder.com/1200x300.png?text=Exceleron+Project+Banner)

**Exceleron** is a full-stack web application designed to transform raw Excel data into beautiful, interactive, and insightful visualizations. Users can upload Excel files, dynamically generate a wide variety of 2D and 3D charts, and receive AI-powered insights to make data-driven decisions effortlessly.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-19-blue?logo=react)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-green?logo=node.js)](https://nodejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)

---

## ✨ Key Features

- **Secure User Authentication**: Complete auth system with signup, login, email verification, and password reset functionality using JWT.
- **Smart File Upload**: Drag-and-drop interface for `.xlsx`, `.xls`, and `.csv` files with intelligent header detection and data validation.
- **Dynamic Chart Generation**:
    - **2D Charts**: Interactive Bar, Line, and Pie charts powered by Chart.js.
    - **3D Visualizations**: Stunning 3D bar charts built with Three.js and React Three Fiber.
- **AI-Powered Insights**: An integrated AI engine analyzes your data to automatically detect trends, patterns, anomalies, and provide actionable recommendations.
- **Comprehensive Dashboard**: A central hub for all activities, including:
    - **File Management**: Upload and process new files.
    - **Analytics Hub**: View and customize charts.
    - **History Center**: Track and revisit past uploads and analyses.
    - **User Profile**: Manage account settings.
- **Secure Admin Panel**: Role-based access control for administrators to manage users and monitor platform activity.
- **Advanced Export Options**: Download charts and reports as PNG or PDF.
- **Modern & Interactive UI**: A sleek, dark-themed interface built with Tailwind CSS and brought to life with animations from Framer Motion and custom WebGL effects.

---

## 🚀 Technologies Used

### Frontend

- **Framework**: [React](https://reactjs.org/) (v19) with [Vite](https://vitejs.dev/)
- **State Management**: [Zustand](https://github.com/pmndrs/zustand)
- **Routing**: [React Router DOM](https://reactrouter.com/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Animations**: [Framer Motion](https://www.framer.com/motion/)
- **Charting**: [Chart.js](https://www.chartjs.org/) & [react-chartjs-2](https://react-chartjs-2.js.org/)
- **3D Graphics**: [Three.js](https://threejs.org/) & [@react-three/fiber](https://docs.pmnd.rs/react-three-fiber/getting-started/introduction)
- **HTTP Client**: [Axios](https://axios-http.com/)
- **File Handling**: [xlsx](https://github.com/SheetJS/sheetjs)

### Backend

- **Runtime**: [Node.js](https://nodejs.org/)
- **Framework**: [Express.js](https://expressjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/)
- **Authentication**: [JSON Web Tokens (JWT)](https://jwt.io/) & [cookie-parser](https://github.com/expressjs/cookie-parser)
- **Password Hashing**: [bcrypt.js](https://github.com/dcodeIO/bcrypt.js)
- **Transactional Emails**: [Brevo (formerly Sendinblue)](https://www.brevo.com/)
- **CORS**: [cors](https://github.com/expressjs/cors)

---

## 🔧 Installation and Setup

Follow these steps to get the project up and running on your local machine.

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) (v18 or later recommended)
- [npm](https://www.npmjs.com/get-npm)
- [MongoDB](https://www.mongodb.com/try/download/community) installed and running.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Excel-Analystics-main.git
cd Excel-Analystics-main/Excel - Analytics
```

### 2. Backend Setup

```bash
# Navigate to the backend directory
cd Backend

# Install dependencies
npm install

# Create a .env file in the Backend directory
touch .env
```

Add the following environment variables to your `.env` file. See the `.env.example` section below for descriptions.

```ini
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
CLIENT_URL=http://localhost:5173
BREVO_API_KEY=your_brevo_api_key
SENDER_EMAIL=your_sender_email@example.com
SENDER_NAME=Exceleron
```

### 3. Frontend Setup

```bash
# Navigate to the frontend directory from the root
cd ../Frontend

# Install dependencies
npm install
```

### 4. Running the Application

1.  **Start the Backend Server**:
    ```bash
    # In the Backend directory
    npm start
    ```
    *(Note: You may need to add a `start` script to `Backend/package.json`: `"start": "node index.js"`)*

2.  **Start the Frontend Development Server**:
    ```bash
    # In the Frontend directory
    npm run dev
    ```

3.  **Open the Application**:
    Open your browser and navigate to `http://localhost:5173`.

---

## ⚙️ Environment Variables (`.env.example`)

This file should be created in the `Backend` directory.

```ini
# The port for the backend server to run on
PORT=5000

# Your MongoDB connection string
MONGO_URI=mongodb://localhost:27017/exceleron

# A secret key for signing JWTs (choose a long, random string)
JWT_SECRET=your_super_secret_jwt_key

# The URL of the frontend application for CORS and email links
CLIENT_URL=http://localhost:5173

# Brevo (or other transactional email service) API Key
BREVO_API_KEY=your_brevo_api_key

# The email address that sends automated emails
SENDER_EMAIL=your_sender_email@example.com

# The name displayed in the sender field of emails
SENDER_NAME=Exceleron
```

---

## 📂 Project Structure

The project is organized as a monorepo with two main directories:

```
.
├── Backend/      # Contains the Node.js and Express.js server
│   ├── controllers/  # Request handling logic
│   ├── db/         # Database connection logic
│   ├── mailtrap/   # Email configuration and templates
│   ├── middleware/ # Express middleware (e.g., token verification)
│   ├── models/     # Mongoose data models
│   ├── routes/     # API routes
│   └── index.js    # Main server entry point
│
├── Frontend/     # Contains the React and Vite client
│   ├── public/     # Static assets
│   └── src/
│       ├── components/ # Reusable UI components
│       ├── DashboardComponents/ # Components specific to the main dashboard
│       ├── pages/      # Page-level components
│       ├── Reactbitzs/ # Special UI effect components
│       ├── store/      # Zustand state management store
│       ├── App.jsx     # Main app component with routing
│       └── main.jsx    # Application entry point
│
└── README.md     # This file
```

---

## 🖼️ Screenshots

*(Add screenshots of your application here to showcase its features.)*

| Login Page | Dashboard | Chart View |
| :---: | :---: | :---: |
| ![Login Page](https://via.placeholder.com/400x300.png?text=Login+Page) | ![Dashboard](https://via.placeholder.com/400x300.png?text=Dashboard) | ![Chart View](https://via.placeholder.com/400x300.png?text=Chart+View) |

---

## 📞 Contact

Your Name - [adityadhanraj.dev@gmail.com](mailto:youremail@example.com)

Project Link: [https://github.com/your-username/Excel-Analystics-main](https://github.com/your-username/Excel-Analystics-main)
