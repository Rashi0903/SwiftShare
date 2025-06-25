# 🚀 SwiftShare

**SwiftShare** is a blazing-fast, secure, and elegant file-sharing platform built for local networks. Whether you're uploading notes or sending multiple PDFs to your friends, SwiftShare lets you upload/download files seamlessly — with passcode protection, time-bound access, and a crisp UI.

---

## ✨ Features

- 🔐 **User Signup/Login** using PHP + MySQL
- 📂 **Multi-file Upload** with single passcode
- 🧠 **One-time Download** or **10-min expiry**
- 💾 **SQLite-based Storage**
- 🧵 **Multi-threaded-style performance** via Flask handling multiple requests
- 🎨 **Modern UI** with animated homepage and responsive design
- 🛡️ **Virus-scan logic stubbed (mock)** for future enhancement

---

## 🛠️ Tech Stack

| Layer         | Technology            |
|---------------|------------------------|
| Frontend      | HTML, CSS, JavaScript  |
| Backend       | Python (Flask)         |
| Auth Module   | PHP + MySQL (XAMPP)    |
| Database      | SQLite (Flask side)    |
| Deployment    | Localhost (XAMPP + Flask) |

---

## 🚀 Project Structure

SwiftShare/
├── auth/ # PHP files (login, signup)
├── backend/ # Flask backend (upload, download routes)
│ ├── app.py
│ └── swiftshare.db
├── frontend/
│ ├── upload.html
│ ├── download.html
│ ├── dashboard.html
│ └── assets/ # CSS, images, etc.
└── README.md


## ⚙️ Setup Instructions

### 🧪 Local Environment

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/SwiftShare.git
   cd SwiftShare
Start XAMPP:

Place the auth/ folder into htdocs/ directory.

Start Apache and MySQL from XAMPP Control Panel.

Import the swiftshare1 database in phpMyAdmin.

Run the Flask App:

bash
Copy
Edit
cd backend
python app.py
Visit Frontend:

Open upload.html, download.html, or dashboard.html from your browser.

🧩 How It Works
Users sign up and log in via PHP.

Once logged in, they’re redirected to a dashboard.

They can upload multiple files → a 6-character passcode is generated.

The passcode is valid for one download OR 10 minutes, whichever comes first.

On download, a ZIP file is delivered and marked "downloaded" in the DB.

Download attempt after that returns ❌ expired/used message.

💡 Future Enhancements
Real Virus Scan with ClamAV or external API

File Encryption (AES)

Email/QR-based sharing

Full cloud deployment (Heroku / AWS)

📜 License
This project is licensed under MIT License. Free to use and improve!
