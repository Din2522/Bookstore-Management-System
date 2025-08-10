# Bookstore Management System

A full-stack web application built with the MERN stack (MongoDB, Express.js, React, Node.js) for managing a bookstore's inventory, orders, and customer interactions.

## Features

### Backend (Node.js + Express + MongoDB)
- User authentication with JWT
- Role-based access control (customer/admin)
- Book management (CRUD operations)
- Order processing
- RESTful API design
- Error handling and validation

### Frontend (React + Redux + Material UI + Framer Motion)
- Responsive design with Material UI components
- Smooth animations with Framer Motion
- User authentication and authorization
- Book browsing with search and filtering
- Shopping cart functionality
- Checkout process
- Admin dashboard for managing books and orders

## Project Structure

```
bookstore-management-system/
│
├── backend/                    # Node.js + Express + MongoDB
│   ├── server.js              # Entry point
│   ├── package.json           # Backend dependencies
│   ├── config/                # Database configuration
│   ├── middleware/            # Authentication and error handling
│   ├── models/                # Mongoose models
│   ├── routes/                # API routes
│   └── controllers/           # Request handlers
│
└── frontend/                  # React + Redux + Material UI + Framer Motion
    ├── package.json           # Frontend dependencies
    ├── public/                # Static assets
    └── src/
        ├── index.js           # Entry point
        ├── App.js             # Main application component
        ├── redux/             # State management
        ├── pages/             # Page components
        ├── components/        # Reusable components
        ├── utils/             # Utility functions
        └── styles/            # Styling and theme
```

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory with the following variables:
   ```env
   NODE_ENV=development
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

4. Start the backend server:
   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open your browser and visit `http://localhost:3000`

## API Endpoints

### Books
- `GET /api/books` - Get all books with pagination
- `GET /api/books/:id` - Get a specific book
- `POST /api/books` - Create a new book (admin only)
- `PUT /api/books/:id` - Update a book (admin only)
- `DELETE /api/books/:id` - Delete a book (admin only)

### Users
- `POST /api/users` - Register a new user
- `POST /api/users/login` - Login user
- `GET /api/users/profile` - Get user profile (authenticated)

### Orders
- `POST /api/orders` - Create a new order (authenticated)
- `GET /api/orders/myorders` - Get logged-in user's orders (authenticated)
- `GET /api/orders/:id` - Get a specific order (authenticated)
- `GET /api/orders` - Get all orders (admin only)
- `PUT /api/orders/:id/status` - Update order status (admin only)

## Technologies Used

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JSON Web Tokens (JWT) for authentication
- Bcrypt.js for password hashing
- Morgan for logging

### Frontend
- React
- Redux Toolkit for state management
- React Router for navigation
- Material UI for UI components
- Framer Motion for animations
- Axios for HTTP requests
- Sass for styling

## Deployment

### Backend
1. Set environment variables on your hosting platform
2. Deploy to platforms like Heroku, Render, or AWS

### Frontend
1. Build the production version:
   ```bash
   npm run build
   ```
2. Deploy the build folder to platforms like Vercel, Netlify, or GitHub Pages

## Contributing
1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a pull request

## License
This project is licensed under the MIT License.

## Contact
For any questions or feedback, please open an issue on GitHub.