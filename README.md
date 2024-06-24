# Google OAuth Authentication Project

## Overview
This project demonstrates the implementation of Google OAuth authentication in a web application. The backend is built using Node.js with Express and Passport.js for authentication, while the frontend is built using React.js.

## Table of Contents
1. [Project Structure](#project-structure)
2. [Backend Setup](#backend-setup)
3. [Frontend Setup](#frontend-setup)
4. [Running the Application](#running-the-application)
5. [Environment Variables](#environment-variables)
6. [Conclusion](#conclusion)

## Project Structure

```
tensergo-project/
├── server/
│   ├── node_modules/
│   ├── passport.js
│   ├── server.js
│   ├── package.json
│   └── .env
└── client/
    ├── node_modules/
    ├── public/
    ├── src/
    │   ├── components/
    │   │   └── Login.js
    │   ├── App.js
    │   ├── index.js
    └── package.json
```

## Backend Setup

### Installation

1. Initialize the Node.js project.
2. Install the necessary dependencies: `express`, `passport`, `passport-google-oauth20`, `express-session`, and `dotenv`.

### Configuration

1. Set up the Express application.
2. Configure session middleware.
3. Initialize Passport and configure it to use the Google OAuth 2.0 strategy.
4. Set up serialization and deserialization of user information.
5. Define authentication routes.

## Frontend Setup

### Installation

1. Initialize the React project using Create React App.
2. Install the necessary dependencies, such as `axios`.

### Components

1. Create a `Login` component with a button that initiates Google OAuth login.
2. Create an `App` component to handle user authentication state and display user information or the login button.

### Authentication Flow

1. User clicks the login button, which redirects to Google for authentication.
2. Google redirects back to the application with an authentication code.
3. The backend exchanges the code for user information and establishes a session.
4. The frontend fetches user information from the backend and displays it.

## Running the Application

1. Start the backend server:
   - Navigate to the `server` directory.
   - Run the server using Node.js.

2. Start the frontend development server:
   - Navigate to the `client` directory.
   - Start the development server using `npm start`.

## Environment Variables

Create a `.env` file in the `server` directory with the following content:

- `GOOGLE_CLIENT_ID`: Your Google Client ID.
- `GOOGLE_CLIENT_SECRET`: Your Google Client Secret.
- `SESSION_SECRET`: A secret key for Express session.
- `PORT`: The port on which the server will run (default is 5000).
