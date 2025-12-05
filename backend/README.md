# Employees-Management Backend API

This is the backend API for the Employees-Management system, built with Node.js, Express.js, and TypeScript. It provides RESTful APIs for managing employee data, authentication, tasks, leaves, skills, and more.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Environment Setup](#environment-setup)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Models](#models)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication (signup, login, password reset)
- Employee management (CRUD operations)
- Task management
- Leave request system
- Holiday management
- Skill management
- Discussion desk/forum
- Project updates
- Test and call management
- Daily status updates
- Admin panel functionalities
- Email notifications
- File uploads

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcrypt
- **File Uploads**: Multer
- **Email**: Nodemailer
- **Scheduling**: node-cron
- **Testing**: Jest, Supertest
- **Development**: Nodemon

## Prerequisites

- Node.js (>=14)
- npm or yarn
- MongoDB (local installation or cloud service like MongoDB Atlas)
- Git

## Installation

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Environment Setup

Create a `.env` file in the backend root directory with the following variables:

```
MONGODB_URL=mongodb://localhost:27017/employees-management
JWT_SECRET_KEY=your-super-secret-jwt-key-here
PORT=5000
BaseUrl=http://localhost:3000
user_Credential=your-email-username@gmail.com
pass_Credential=your-email-password
```

- `MONGODB_URL`: MongoDB connection string
- `JWT_SECRET_KEY`: Secret key for JWT token generation
- `PORT`: Port for the server (default: 5000)
- `BaseUrl`: Frontend URL for CORS
- `user_Credential`: Email username for sending notifications
- `pass_Credential`: Email password/app password

## Running the Application

### Development Mode
```bash
npm start
```
This starts the server with nodemon for automatic restarts on file changes.

### Production Mode
```bash
npm run build
npm run start:prod
```

## API Endpoints

The API is organized into the following main routes:

### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/login` - User login
- `POST /auth/forgot-password` - Request password reset
- `POST /auth/reset-password` - Reset password

### Users
- `GET /users` - Get all users
- `GET /users/:id` - Get user by ID
- `PUT /users/:id` - Update user
- `DELETE /users/:id` - Delete user

### Tasks
- `GET /tasks` - Get all tasks
- `POST /tasks` - Create new task
- `PUT /tasks/:id` - Update task
- `DELETE /tasks/:id` - Delete task

### Leaves
- `GET /leaveSection` - Get leave requests
- `POST /leaveSection` - Apply for leave
- `PUT /leaveSection/:id` - Update leave request
- `DELETE /leaveSection/:id` - Delete leave request

### Holidays
- `GET /holiDays` - Get holidays
- `POST /holiDays` - Add holiday
- `PUT /holiDays/:id` - Update holiday
- `DELETE /holiDays/:id` - Delete holiday

### Skills
- `GET /EditSkills` - Get skills
- `POST /EditSkills` - Add skill
- `PUT /EditSkills/:id` - Update skill
- `DELETE /EditSkills/:id` - Delete skill

### Discussion Desk
- `GET /discussion_desk` - Get discussions
- `POST /discussion_desk` - Create discussion
- `PUT /discussion_desk/:id` - Update discussion
- `DELETE /discussion_desk/:id` - Delete discussion

### Projects
- `GET /project` - Get projects
- `POST /project` - Create project
- `PUT /project/:id` - Update project
- `DELETE /project/:id` - Delete project

### Tests and Calls
- `GET /tests` - Get tests
- `POST /tests` - Create test
- `GET /calls` - Get calls
- `POST /calls` - Create call

### Personal Info
- `GET /editPesonalInfo` - Get personal info
- `PUT /editPesonalInfo` - Update personal info

### Status
- `GET /changeStatus` - Get status
- `PUT /changeStatus` - Update status

## Models

The application uses the following Mongoose models:

- **User**: Employee/user information
- **Task**: Task details and assignments
- **Leave**: Leave requests and approvals
- **Holiday**: Company holidays
- **Skill**: Employee skills
- **Discussion**: Forum discussions
- **Project**: Project information
- **Test**: Interview tests
- **Call**: Interview calls
- **Status**: Daily status updates

## Testing

Run tests using Jest:

```bash
npm test
```

Tests are located in `src/tests/` directory.

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and add tests
4. Run tests: `npm test`
5. Commit changes: `git commit -am 'Add feature'`
6. Push to branch: `git push origin feature-name`
7. Create a pull request

## License

This project is licensed under the ISC License.
