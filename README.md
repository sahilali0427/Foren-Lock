# 🔐 ForenLock: Intelligent Locker

ForenLock is a secure web-based digital file management system designed to store, monitor, and manage digital files securely.

The system combines **file integrity verification, SHA-256 hashing, face authentication, user management, storage monitoring, and forensic activity tracking** in a single web application.

---

## 🚀 Features

### 🔐 Secure Authentication
- User registration and login
- Password hashing using Werkzeug
- Face recognition-based second-step verification
- Session-based authentication
- Role-based access control

### 👤 Face Authentication
- Face registration during account creation
- Webcam-based face verification
- Face encoding stored securely in MySQL
- Face matching using the `face_recognition` library

### 📁 File Management
- Upload digital files
- Store files separately for each user
- Download uploaded files
- View uploaded files
- File status monitoring
- Unique file names using UUID

### 🛡️ File Integrity Verification
- SHA-256 hash generated when a file is uploaded
- Original hash stored in the database
- File integrity can be checked against the stored hash
- Files can be identified as:
  - `SAFE`
  - `TAMPERED`

### 🕒 Forensic Timeline
The forensic timeline records important file activities such as:

- File Uploaded
- File Downloaded
- Other recorded file-related activities

This provides a chronological record of activities performed on files.

### 👨‍💼 Admin Panel
The admin can:

- View total users
- View total files
- View registered users
- View user roles
- Monitor user storage usage
- Delete users

The first registered account is automatically assigned the `admin` role.

### 💾 Storage Management
- Individual user storage tracking
- 2 GB storage limit per user
- Storage usage displayed in MB
- Storage progress bar in the admin panel

---

## 🛠️ Technologies Used

### Backend
- Python
- Flask

### Frontend
- HTML5
- CSS3
- JavaScript

### Database
- MySQL
- Flask-MySQLdb

### Security
- Werkzeug password hashing
- SHA-256 file hashing
- Flask sessions
- Role-based access control

### Face Recognition
- face_recognition
- NumPy
- Pillow
- OpenCV-compatible image processing

### Python Libraries
- `uuid`
- `hashlib`
- `pickle`
- `base64`
- `os`
- `shutil`

---

## 🏗️ Project Structure

```text
Foren-Lock/
│
├── app.py
├── requirements.txt
├── README.md
│
├── static/
│   ├── admin.css
│   ├── auth.css
│   ├── dashboard.css
│   ├── face.css
│   ├── home.css
│   ├── my_files.css
│   ├── timeline.css
│   └── upload.css
│
├── templates/
│   ├── admin.html
│   ├── dashboard.html
│   ├── face_register.html
│   ├── face_verify.html
│   ├── home.html
│   ├── login.html
│   ├── my_files.html
│   ├── signup.html
│   ├── timeline_all.html
│   ├── timeline.html
│   └── upload.html
│
└── uploads/
    └── User file storage
