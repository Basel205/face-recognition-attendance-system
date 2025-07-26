# Smart Attendance System

This project is a **Smart Attendance System** that uses face recognition to automate attendance tracking.  
It consists of a Python Flask backend and a React frontend.

## Features
- Student registration with webcam image capture  
- Face encoding and model training using machine learning  
- Attendance session management with start/stop camera  
- Attendance tracking and reporting via a web interface  

## Technologies Used
- **Backend:** Python, Flask, Pandas, OpenCV (for face recognition)  
- **Frontend:** React, Vite, CSS  
- **Data Storage:** CSV files for attendance, sessions, and registered students  
- **Machine Learning:** Face encoding and training scripts in Python  

## Project Structure
```
ATTENDANCE-SYSTEM
├── app.py                  # Flask backend entry
├── ml_model/               # Python scripts for face recognition
├── src/                    # React frontend source
├── data/                   # CSV files, images (not included for privacy)
├── public/                 # Public assets for frontend
├── requirements.txt        # Python dependencies
├── package.json            # Frontend dependencies
├── .gitignore
└── README.md
```

## Setup Instructions
1. Install Python dependencies (preferably in a virtual environment):
   ```
   pip install -r requirements.txt
   ```
2. Install Node.js dependencies:
   ```
   npm install
   ```
3. Run the backend server:
   ```
   python app.py
   ```
4. Run the frontend development server:
   ```
   npm run dev
   ```
5. Access the frontend at:
   ```
   http://localhost:5174
   ```

## Dataset Preparation
For privacy reasons, actual student images and CSV data are not included in this repository.  
To run the system, create your own dataset in the following structure:

```
data/
├── images/
│   ├── Person_A/
│   │   ├── img1.jpg
│   │   └── img2.jpg
│   ├── Person_B/
│   │   ├── img1.jpg
│   │   └── img2.jpg
│   └── ...
└── registered_students.csv
```

**Example `registered_students.csv`:**
```
name,student_id
Person_A,001
Person_B,002
```

When you run `capture_images.py` and `train_model.py`, the system will generate:
- `data/encodings.pickle` (face encodings)
- `data/attendance.csv` (attendance records)
- `data/sessions.csv` (session data)

## Git Ignore Recommendations
The following files and folders are recommended to be ignored in `.gitignore`:

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
- This project is primarily intended for local use and testing.
