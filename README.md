# 🔧 QuickFix

> Paste your code. Get an instant AI review.

QuickFix reviews your code using Google Gemini API and tells you 
exactly what's wrong, what could be better, and shows you a 
cleaner version — in seconds.

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Stack](https://img.shields.io/badge/Stack-MERN%20%2B%20Gemini-blue)

---

## What it does

You paste a code snippet, select your language, and QuickFix gives you:

- 🐛 Bugs found in your code
- ⚠️ Best practice violations
- 📊 A quality score out of 10
- ✨ A cleaner, refactored version of your code
- 📁 History of all your past reviews

---

## Built with

- **React + Tailwind** — frontend
- **Node.js + Express** — backend API
- **Google Gemini API** — AI code analysis (free tier)
- **MongoDB** — storing review history
- **JWT** — authentication
- **Monaco Editor** — VS Code-like code input

---

## Project Structure
quickfix/
├── client/              # React app
│   └── src/
│       ├── components/
│       │   ├── Editor/      # code input + language picker
│       │   ├── Review/      # feedback + score display
│       │   ├── History/     # past reviews
│       │   └── Auth/        # login + register
│       └── App.jsx
│
└── server/              # Express backend
├── config/          # database connection
├── models/          # User, Review schemas
├── routes/          # API routes
├── controllers/     # business logic
├── middleware/      # JWT auth + rate limiter
└── services/
└── gemini.service.js  # prompt engineering + response parsing

---

## Running locally

**You'll need:**
- Node.js v18+
- MongoDB
- Gemini API key → get it free at [aistudio.google.com](https://aistudio.google.com)

```bash
git clone https://github.com/mohitcodes12/quickfix.git
cd quickfix

cd server && npm install
cd ../client && npm install
```

Create a `.env` in `/server`:

```env
PORT=3001
MONGO_URI=your_mongo_url
JWT_SECRET=your_secret
GEMINI_API_KEY=your_gemini_key
```

```bash
# run backend
cd server && npm run dev

# run frontend
cd client && npm run dev
```

App runs at `http://localhost:5173`

---

## How the AI review works

1. You paste code + pick a language
2. Backend builds a prompt and sends it to Gemini
3. Gemini returns structured JSON with bugs, suggestions, score
4. Frontend parses and displays it cleanly
5. Review gets saved to your history in MongoDB

---

## Progress

- [x] Folder structure and project setup
- [ ] Auth system (JWT)
- [ ] Gemini API integration + prompt engineering
- [ ] Code quality score UI
- [ ] Bug and suggestion display
- [ ] Rate limiting
- [ ] Review history + filters
- [ ] Monaco Editor
- [ ] Deploy on Railway + Vercel

---



Made by [Mohit Kumar Verma](https://github.com/mohitcodes12)
