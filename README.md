# Smart Attendance System

This project is a Smart Attendance System that uses face recognition to automate attendance tracking. It consists of a Python Flask backend and a React frontend.

## Features

- Student registration with webcam image capture
- Face encoding and model training using machine learning
- Attendance session management with start/stop camera
- Attendance tracking and reporting via a web interface

## Technologies Used
- Backend: Python, Flask, Pandas, OpenCV (for face recognition)
- Frontend: React, Vite, CSS
- Data storage: CSV files for attendance, sessions, and registered students
- Machine Learning: Face encoding and training scripts in Python

## Setup Instructions

1. Install Python dependencies (preferably in a virtual environment).
2. Install Node.js dependencies with `npm install`.
3. Run the backend server: `python app.py`.
4. Run the frontend dev server: `npm run dev`.
5. Access the frontend at `http://localhost:5174`.

## Git Ignore Recommendations

Add the following to your `.gitignore` file to avoid committing unnecessary or sensitive files:

```
# Python
__pycache__/
*.pyc
*.pyo
*.pyd
env/
venv/
.env

# Node
node_modules/
dist/
build/

# Data files
data/attendance.csv
data/sessions.csv
data/registered_students.csv
data/encodings.pickle

# Uploaded images and generated files
data/images/
data/uploads/

# IDE and OS files
.vscode/
.DS_Store
Thumbs.db
```

## Notes

- Ensure you do not commit large data files or images to the repository.
- Use environment variables or config files for sensitive information if added later.
- This project is intended for local use and testing.
