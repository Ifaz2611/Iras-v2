University Student Records Management

A full-stack CRUD application for managing student records. This project allows users to view, add, update, and delete student records. It features authentication, role-based access control, and data export functionality, providing a simple and efficient way to manage student data.

Features

Authentication: Users can log in and register with a secure authentication system.

Role-based Access Control: Different roles (e.g., admin, student) have different levels of access to student records.

CRUD Operations: Perform Create, Read, Update, and Delete operations on student records.

Data Export: Export student data in various formats.

Responsive UI: Built with Next.js and styled components for a smooth and responsive experience.

Tech Stack

Frontend: Next.js, React, Tailwind CSS

Backend: Node.js, Express

Database: MongoDB (or other database of choice)

Authentication: JWT (JSON Web Tokens)

Role Management: Middleware to protect routes based on user roles

Deployment: Vercel (Frontend) & Heroku (Backend)

Setup
1. Clone the repository:
git clone https://github.com/yourusername/university-student-records.git
cd university-student-records

2. Install dependencies:
npm install

3. Environment Variables:

Create a .env.local file in the root directory and add the following:

NEXT_PUBLIC_API_URL=http://localhost:5000/api
DATABASE_URL=mongodb://localhost:27017/university_db
JWT_SECRET=your_secret_key

4. Running the development server:
npm run dev


The application will be running at http://localhost:3000.

5. Run the Backend Server:

In a separate terminal window, navigate to the backend directory (if using a separate backend) and run:

npm run start


Now your backend API should be available at http://localhost:5000.

Usage
Roles

Admin: Can add, update, and delete student records.

Student: Can only view their own record.

Authentication

Use the login form to authenticate with registered credentials.

Once logged in, users are redirected to the dashboard with relevant permissions based on their role.

API Endpoints

POST /api/auth/register – Register a new user

POST /api/auth/login – Log in to an existing account

GET /api/students – Get all student records (Admin only)

POST /api/students – Add a new student record (Admin only)

PUT /api/students/:id – Update a student record (Admin only)

DELETE /api/students/:id – Delete a student record (Admin only)

Data Export

Admins can export student records in CSV format from the dashboard.

Contributing

Fork the repository

Create your branch (git checkout -b feature-name)

Commit your changes (git commit -m 'Add feature')

Push to the branch (git push origin feature-name)

Open a Pull Request

License

This project is licensed under the MIT License.