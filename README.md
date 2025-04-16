# Full-Stack To-Do List App (Django + React)

A robust and user-friendly To-Do List application built with Django and React, designed to help users efficiently manage their tasks and stay organized. It incorporates secure JWT authentication, enabling personalized task management for each user.

Features:
- JWT Authentication (Login, Register, Token Refresh)
- Task Management (Create, Read, Update, Delete)
- User-Specific To-Dos
- REST API with Django REST Framework
- Modern React Frontend
- Real-Time UI Updates with Axios

Project Structure:
your-project/
├── backend/        # Django API (DRF, JWT, Auth, Tasks)
├── frontend/       # React App (UI, Auth, API Integration)
├── .gitignore
├── README.md

Tech Stack:
- Backend: Django, Django REST Framework, SimpleJWT, CORS Headers
- Frontend: React, React Router, Axios, JWT Auth Handling

Backend Setup:
1. Navigate to the backend folder:
   cd backend
2. Create a virtual environment:
   python -m venv venv
3. Activate it:
   source venv/bin/activate  (Windows: venv\Scripts\activate)
4. Install dependencies:
   pip install -r requirements.txt
5. Run migrations:
   python manage.py migrate
6. Start the server:
   python manage.py runserver
7. (Optional) Create a superuser:
   python manage.py createsuperuser

Frontend Setup:
1. Navigate to the frontend folder:
   cd frontend
2. Install packages:
   npm install
3. Start the React dev server:
   npm start

Ensure:
- Django backend is running at http://localhost:8000
- React frontend is running at http://localhost:3000

Authentication (JWT):
- Login and register via `/api/token/` and `/api/register/`
- Tokens are saved in localStorage or memory on the frontend
- For protected endpoints, send the access token as:
  Authorization: Bearer <your_access_token>

API Overview:
POST   /api/register/           - Register new user
POST   /api/token/              - Obtain JWT tokens (login)
POST   /api/token/refresh/      - Refresh access token
GET    /api/tasks/              - List all user tasks
POST   /api/tasks/              - Create a new task
PUT    /api/tasks/<id>/         - Update a task
DELETE /api/tasks/<id>/         - Delete a task
