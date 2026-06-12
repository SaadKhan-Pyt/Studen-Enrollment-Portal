# Student Portal Full Stack Web Application

This project includes:

- React JS, CSS3, Fetch API, and React Router on the frontend
- Django, Django REST Framework, and SQLite on the backend
- Login/register authentication
- Protected CRUD operations for students, courses, and enrollments
- Form validation, API error handling, responsive layouts, and navigation routing

## Project Structure

```text
Student Portal Project/
├── backend/
│   ├── manage.py
│   ├── requirements.txt
│   ├── student_portal/
│   └── portal/
└── frontend/
    ├── package.json
    ├── index.html
    └── src/
```

## Run The Project In VS Code

Open this folder in VS Code:

```bash
code "/Users/apple/Documents/Student Portal Project"
```

### 1. Start The Backend

Open a VS Code terminal:

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

The backend will run at:

```text
http://127.0.0.1:8000
```

Optional admin user:

```bash
python manage.py createsuperuser
```

Admin panel:

```text
http://127.0.0.1:8000/admin/
```

### 2. Start The Frontend

Open a second VS Code terminal:

```bash
cd frontend
npm install
npm run dev
```

The frontend will run at:

```text
http://127.0.0.1:5173
```

### 3. Use The App

1. Register a new account.
2. Add student records.
3. Add course records.
4. Create enrollments by selecting a student and course.
5. Edit and delete records from each page.

## API Endpoints

Auth:

```text
POST /api/auth/register/
POST /api/auth/login/
POST /api/auth/logout/
GET  /api/auth/me/
```

CRUD:

```text
GET    /api/students/
POST   /api/students/
PUT    /api/students/<id>/
DELETE /api/students/<id>/

GET    /api/courses/
POST   /api/courses/
PUT    /api/courses/<id>/
DELETE /api/courses/<id>/

GET    /api/enrollments/
POST   /api/enrollments/
PUT    /api/enrollments/<id>/
DELETE /api/enrollments/<id>/
```

Protected API requests use this header:

```text
Authorization: Token your_token_here
```

## Submission Notes

The PDF asks for:

- GitHub link
- Screenshots of the output
- Group member names

Suggested Git commands:

```bash
git add .
git commit -m "Build student portal full stack app"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## Troubleshooting

If the frontend says the API is not reachable, make sure the Django backend is running on `http://127.0.0.1:8000`.

If migrations fail, make sure your backend virtual environment is activated and dependencies are installed.
