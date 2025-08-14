# 🚀 SwiftShare


**SwiftShare** is a blazing-fast, secure, and elegant file-sharing platform built for **local networks**.  
Whether you're uploading lecture notes or sending multiple PDFs to friends, SwiftShare makes sharing effortless — with **passcode protection**, **time-bound access**, and a **modern UI**.

---

## ✨ Features
- 🔐 **User Signup/Login** — PHP + MySQL authentication
- 📂 **Multi-file Upload** — Share multiple files with a single passcode
- ⏳ **One-time Download or 10-min Expiry**
- 💾 **SQLite-based Storage** — Lightweight & efficient
- ⚡ **Fast Performance** — Flask backend handling multiple requests
- 🎨 **Responsive Design** — Modern animations & UI
- 🛡️ **Virus Scan Ready** — Stubbed logic for future use

---

## 🛠️ Tech Stack

| Layer        | Technology           |
|--------------|----------------------|
| Frontend     | HTML, CSS, JavaScript |
| Backend      | Python (Flask)        |
| Auth Module  | PHP + MySQL (XAMPP)   |
| Database     | SQLite (Flask side)   |
| Deployment   | Localhost (XAMPP + Flask) |

---

## 📂 Project Structure
```plaintext
SwiftShare/
├── auth/                  # PHP authentication module
│   ├── login.php           # User login
│   ├── signup.php          # User registration
│   ├── logout.php          # End user session
│   ├── config.php          # MySQL connection setup
│   └── swiftshare1.sql     # MySQL DB export (import in phpMyAdmin)
│
├── backend/                # Flask backend
│   ├── app.py               # Main Flask server
│   ├── swiftshare.db        # SQLite database for file metadata
│   ├── uploads/             # Uploaded files storage
│   └── utils/               # Helper scripts (future use)
│
├── frontend/               # User Interface
│   ├── upload.html          # File upload page
│   ├── download.html        # File download page
│   ├── dashboard.html       # User dashboard
│   ├── index.html           # Landing page (animated)
│   └── assets/
│       ├── css/             # Stylesheets
│       │   ├── style.css
│       │   └── dashboard.css
│       ├── js/              # JavaScript files
│       │   ├── main.js
│       │   └── upload.js
│       ├── images/          # Icons, backgrounds
│       └── animations/      # Optional animation assets
│
└── README.md               # Project documentation
```
---
## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Rashi0903/SwiftShare.git
cd SwiftShare
```
### 2️⃣ Start XAMPP (Apache + MySQL)

Move the auth/ folder into your htdocs/ directory.

Start Apache and MySQL from the XAMPP Control Panel.

Import swiftshare1.sql into phpMyAdmin.

### 3️⃣ Run the Flask Backend
```bash
cd backend
python app.py
```
4️⃣ Access the Frontend
Open upload.html, download.html, or dashboard.html directly in your browser.


---

```markdown
## 🧩 How It Works

### 1. **User Authentication**
Users sign up and log in via the **PHP + MySQL** module.

### 2. **File Upload**
- Multiple files can be uploaded at once.
- A **6-character passcode** is generated.

### 3. **Download Rules**
- Passcode works **once** OR **for 10 minutes**, whichever comes first.
- On download, files are **zipped** and marked as **used**.
- Expired/used passcodes → ❌ "Access Denied".
```

## 💡 Future Enhancements
- 🔍 **Real Virus Scan** — Integrate with ClamAV or an external API.
- 🔐 **AES File Encryption** — Add end-to-end encryption for files.
- 📩 **Email/QR Code Sharing** — Share links with email or scannable codes.
- ☁️ **Cloud Deployment** — Deploy to platforms like Heroku or AWS.
