# 🔧 QuickFix

An AI-powered code review tool that accepts code snippets in multiple 
languages and instantly returns structured feedback on bugs, best 
practice violations, code quality score, and refactoring suggestions 
— powered by Google Gemini API.

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Tech](https://img.shields.io/badge/Stack-MERN%20%2B%20Gemini-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🚀 Live Demo
> Coming soon — deployment in progress

---

## ✨ Features

- 🤖 AI-powered code review via Google Gemini API
- 🌐 Supports multiple programming languages
- 🐛 Bug detection and best practice violations
- 📊 Code quality score out of 10
- ✨ Refactored code suggestions
- 🚦 Server-side rate limiting per user
- 📁 Review history with filter by language and date
- 📱 Fully responsive UI

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React | UI framework |
| Tailwind CSS | Styling |
| Monaco Editor | Code input editor (VS Code like) |

### Backend
| Technology | Purpose |
|---|---|
| Node.js + Express | REST API server |
| Google Gemini API | AI code analysis |
| MongoDB + Mongoose | Review history storage |
| JWT + bcrypt | Authentication & security |
| Express Rate Limit | API abuse prevention |

---

## 📁 Project Structure
quickfix/
│
├── client/                   # React frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── Editor/       # Code input, language selector
│   │   │   ├── Review/       # Feedback display, quality score
│   │   │   ├── History/      # Past reviews, filters
│   │   │   └── Auth/         # Login, Register
│   │   └── App.jsx
│
├── server/                   # Node.js backend
│   ├── config/               # DB connection
│   ├── models/               # User, Review schemas
│   ├── routes/               # Auth, Review API routes
│   ├── controllers/          # Business logic
│   ├── middleware/           # JWT + rate limiter
│   └── services/
│       └── gemini.service.js # Gemini prompt + response parsing

---

## ⚙️ Getting Started

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)
- Google Gemini API Key (free at [aistudio.google.com](https://aistudio.google.com))

### Installation

```bash
# Clone the repo
git clone https://github.com/mohitcodes12/quickfix.git
cd quickfix

# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

### Environment Variables

Create a `.env` file inside `/server`:

```env
PORT=3001
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
```

### Run the App

```bash
# Start server (from /server)
npm run dev

# Start client (from /client)
npm run dev
```

Open `http://localhost:5173` in your browser.

---

## 🤖 How It Works
User pastes code + selects language
↓
Frontend sends code to backend API
↓
Backend checks rate limit (max X requests/hour per user)
↓
Google Gemini API analyzes code via dynamic prompt
↓
Gemini returns structured JSON response:
{
score: 7/10,
bugs: [...],
bestPracticeViolations: [...],
suggestions: [...],
refactoredCode: "..."
}
↓
Response parsed + displayed in clean UI
↓
Review saved to MongoDB for history

---

## 🗺️ Development Roadmap

- [x] Project setup and folder structure
- [ ] User authentication (Register/Login with JWT)
- [ ] Google Gemini API integration with prompt engineering
- [ ] Structured JSON response parsing
- [ ] Code quality score display
- [ ] Bug and suggestion display UI
- [ ] Server-side rate limiting
- [ ] Review history with MongoDB aggregation
- [ ] Filter reviews by language and date
- [ ] Monaco Editor integration
- [ ] Deployment (Railway + Vercel)

---

## 📸 Screenshots
> Coming soon

---

## 🤝 Connect

**Mohit Kumar Verma**
- GitHub: [@mohitcodes12](https://github.com/mohitcodes12)
- LinkedIn: [mohit-kumar-verma](https://www.linkedin.com/in/mohit-kumar-verma-b45586267/)
- Email: mohit.kverma12@gmail.com

---

> ⭐ Star this repo if you find it interesting!
