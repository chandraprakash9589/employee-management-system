# Employees-Management

A comprehensive MERN stack application for managing employee-related operations in an organization. This system provides features for employee authentication, task management, leave requests, holiday tracking, skill management, discussion forums, project updates, and more.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Secure signup, login, and password reset functionality.
- **Employee Management**: View and edit personal information, manage user profiles.
- **Task Management**: Create, update, and track employee tasks.
- **Leave Management**: Apply for leaves, view leave history, and admin approval.
- **Holiday Tracking**: Manage and display company holidays.
- **Skill Management**: Add, edit, and display employee skills.
- **Discussion Desk**: Internal forum for employee discussions.
- **Project Updates**: Manage and update project information.
- **Test and Call Management**: Handle interview tests and calls.
- **Daily Status**: Send and view daily status updates.
- **Admin Panel**: Administrative features for managing users, leaves, skills, etc.

## Tech Stack

- **Frontend**: React.js, React Router, Axios, Bootstrap, Formik, React Toastify
- **Backend**: Node.js, Express.js, TypeScript, MongoDB with Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Other**: Multer for file uploads, Nodemailer for emails, Cron jobs

## Architecture

The application follows a MERN stack architecture:

- **Frontend**: React application handling user interface and interactions.
- **Backend**: Express.js server with TypeScript, providing RESTful APIs.
- **Database**: MongoDB for data storage.
- **Authentication**: JWT-based authentication with middleware.

## Prerequisites

- Node.js (>=14)
- npm or yarn
- MongoDB (local or cloud instance)
- Git

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/employees-management.git
   cd employees-management
   ```

2. Install backend dependencies:
   ```bash
   cd backend
   npm install
   ```

3. Install frontend dependencies:
   ```bash
   cd ../frontend
   npm install
   ```

4. Set up environment variables (see Environment Variables section).

5. Start the backend server:
   ```bash
   cd backend
   npm start
   ```

6. Start the frontend application:
   ```bash
   cd frontend
   npm start
   ```

The application will be running at `http://localhost:3000` for frontend and `http://localhost:5000` for backend.

## Usage

1. Open the application in your browser at `http://localhost:3000`.
2. Sign up or log in as an employee or admin.
3. Navigate through the dashboard to access various features like tasks, leaves, skills, etc.
4. Admins can access the admin panel for additional management features.

## Environment Variables

### Backend (.env in backend/ directory)
```
MONGODB_URL=mongodb://localhost:27017/employees-management
JWT_SECRET_KEY=your-jwt-secret-key
PORT=5000
BaseUrl=http://localhost:3000
user_Credential=your-email-username
pass_Credential=your-email-password
```

### Frontend (.env in frontend/ directory)
```
REACT_APP_BASE_URL=http://localhost:5000
```

## API Documentation

The backend provides RESTful APIs. Refer to `backend/README.md` for detailed API endpoints and usage.

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Submit a pull request.

## License

This project is licensed under the ISC License.
