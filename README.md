# 🤖 AI Code Reviewer

An AI-powered Pull Request Review Assistant that automatically analyzes GitHub PRs, detects bugs & security vulnerabilities, and generates intelligent review comments in real-time using Google Gemini 2.5 Flash.

## 🌐 Live Demo

| Service        | Link                                                 |
| -------------- | ---------------------------------------------------- |
| 🏠 Home        | https://ai-code-reviewer-p24m.onrender.com           |
| 📊 Dashboard   | https://ai-code-reviewer-p24m.onrender.com/dashboard |
| 📡 Reviews API | https://ai-code-reviewer-p24m.onrender.com/reviews   |

---

## ✨ Features

### 🔍 AI-Powered PR Review

Reviews Pull Requests automatically and detects:

* Security vulnerabilities
* Logic bugs
* Performance issues
* Code smells
* Best practice violations

### 💬 Smart GitHub Comments

Posts AI-generated review comments directly on Pull Requests.

Supports:

* General review summaries
* Line-by-line issue comments
* Severity tagging

### 📊 Interactive Dashboard

Beautiful dark-themed dashboard with:

* PR analytics
* Severity tracking
* Trend charts
* Review history
* AI-generated summaries

### ❓ Ask AI About Review

Developers can:

* Ask questions about detected issues
* Request explanations in beginner-friendly language
* Understand vulnerabilities clearly

**Example:**

> Why is this SQL injection dangerous?

### 🔧 AI Generate Fix

AI automatically suggests:

* Corrected code
* Safer implementations
* Optimized alternatives
* Best practice fixes

### ☁️ Cloud Deployment

* Fully deployed on Render
* Runs 24/7
* No local machine required

---

## 🧠 What the AI Detects

| Severity  | Examples                                               |
| --------- | ------------------------------------------------------ |
| 🔴 HIGH   | SQL Injection, exposed API keys, hardcoded passwords   |
| 🟡 MEDIUM | Logic errors, missing validations, edge-case failures  |
| 🟢 LOW    | Unused imports, formatting issues, minor optimizations |

---

## 🏗️ System Architecture

```text
Developer Opens Pull Request
              ↓
GitHub Webhook Triggered
              ↓
FastAPI Backend Receives Event
              ↓
GitHub API Fetches Changed Files
              ↓
Code Diff Sent to Gemini AI
              ↓
AI Generates Review
              ↓
Comments Posted Back to GitHub
              ↓
Review Stored in SQLite Database
              ↓
Dashboard Displays Analytics
```

---

## 📸 Dashboard Highlights

### 📈 Analytics

* Total PRs reviewed
* High / Medium / Low issue counts
* Severity trend graph

### 📋 PR Review Cards

Each review contains:

* PR title
* Repository info
* Verdict badge
* Severity pills
* Expandable full AI review

### 🤖 AI Assistant

* Ask questions about reviews
* Generate corrected code instantly

---

## 🛠️ Tools & Technologies Used

| Category             | Tools / Technologies    |
| -------------------- | ----------------------- |
| Backend Framework    | FastAPI                 |
| Programming Language | Python                  |
| AI Model             | Google Gemini 2.5 Flash |
| Database             | SQLite                  |
| ORM                  | SQLAlchemy              |
| API Communication    | Requests                |
| Frontend             | HTML, CSS, JavaScript   |
| Charts               | Chart.js                |
| Markdown Rendering   | Marked.js               |
| Cloud Deployment     | Render.com              |
| Version Control      | Git & GitHub            |
| Webhook Integration  | GitHub Webhooks         |
| Local Testing        | ngrok                   |
| Server               | Uvicorn                 |

---

## ⚙️ Tech Stack

| Technology              | Purpose              |
| ----------------------- | -------------------- |
| Python                  | Backend Language     |
| FastAPI                 | API Framework        |
| Google Gemini 2.5 Flash | AI Code Analysis     |
| GitHub Webhooks         | PR Event Integration |
| SQLAlchemy              | ORM                  |
| SQLite                  | Database             |
| Chart.js                | Dashboard Charts     |
| Marked.js               | Markdown Rendering   |
| Render.com              | Cloud Hosting        |

---

## 🚀 Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/eshivani07/AI-Code-Reviewer.git
cd AI-Code-Reviewer
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Add Environment Variables

Create a `.env` file:

```env
GITHUB_TOKEN=your_github_token
GEMINI_API_KEY=your_gemini_api_key
```

### 4️⃣ Run Server

```bash
uvicorn main:app --reload
```

### 5️⃣ Start ngrok (Local Testing)

```bash
ngrok http 8000
```

---

## 🔗 GitHub Webhook Setup

Go to:

```text
Repository → Settings → Webhooks → Add Webhook
```

### Configuration

| Field        | Value                    |
| ------------ | ------------------------ |
| Payload URL  | https://your-url/webhook |
| Content Type | application/json         |
| Events       | Pull Requests            |

---

## 🛡️ Branch Protection (Optional)

To block merging unsafe PRs:

```text
Repository Settings
    ↓
Branches
    ↓
Branch Protection Rules
    ↓
Require Status Checks Before Merging
```

---

## 📁 Project Structure

```text
AI-Code-Reviewer/
│
├── main.py
├── requirements.txt
├── render.yaml
├── README.md
├── reviews.db
└── .gitignore
```

---

## 📌 Example AI Review

```text
[HIGH] SQL Injection Vulnerability
Fix: Use parameterized queries instead of string concatenation.

[MEDIUM] Missing Error Handling
Fix: Add try-except block around API call.

[LOW] Unused Import
Fix: Remove unused import statement.
```

---

## 🔮 Future Improvements

* AI Quality Score
* Multi-language support
* AI-generated test cases
* Team analytics
* GitLab integration
* Developer learning assistant

---

## ⭐ Project Goal

Reduce manual code review effort using AI while improving code quality, security, and developer productivity.
