# Interview AI – GenAI Interview Preparation System

A full-stack AI-powered platform that analyzes a candidate’s resume against a target job description to generate personalized interview strategies, skill gap insights, and preparation roadmaps.

Upload your **resume** and a **targeted job description** and the app generates an interview strategy report including:

- **Match score** between your profile and the role
- **Skill gaps** (what’s missing / needs improvement)
- **Technical questions** an interviewer may ask for that role
- **Behavioral questions** tailored to the job expectations
- A **roadmap / preparation plan** to close gaps efficiently

The project is built as a full-stack app (React + Node/Express) and uses a GenAI model (Google GenAI) to produce **structured, validated outputs** (to reduce hallucinations and keep results consistent).


---

## ✨ Features

- 📄 **Resume + Job Description Analysis**
  - Extracts and understands structured data from resumes (PDF)
  - Compares with job requirements to evaluate alignment

- 📊 **Match Score & Skill Gap Detection**
  - Computes relevance between candidate profile and job role
  - Identifies missing skills and improvement areas

- 🧠 **AI-Generated Interview Preparation**
  - **Technical Questions** tailored to the role
  - **Behavioral Questions** based on profile context
  - **Preparation Roadmap** for targeted improvement

- 🤖 **Structured GenAI Output**
  - Ensures consistent, validated AI responses
  - Avoids hallucinations via controlled prompting

- 🔐 **Authentication System**
  - Secure login/signup with JWT-based authentication

- 📁 **File Upload & Parsing**
  - Resume upload using Multer
  - PDF parsing via pdf-parse

---

## 🏗️ Architecture Overview

Frontend (React + Vite) <br/>
        ↓ <br/>
Backend (Express API) <br/>
        ↓ <br/>
Services Layer (AI + Processing) <br/>
        ↓ <br/>
MongoDB (User + Data Storage)

---

## Demo flow

1. User signs up / logs in
2. User uploads a resume + job description
3. Backend analyzes both and generates:
   - match score
   - skill-gap analysis
   - technical questions
   - behavioral questions
   - preparation roadmap


---

## 🛠️ Tech Stack

### Frontend
- React
- Vite
- Axios
- React Router

### Backend
- Node.js
- Express
- MongoDB + Mongoose
- JWT Authentication
- Zod (validation)

### AI & Processing
- Google GenAI (@google/genai)
- PDF parsing (pdf-parse)
- File uploads (Multer)
- Optional automation (Puppeteer)

---

## ⚙️ Setup

### Backend

```bash
cd Backend
npm install
```

Create `.env`:

```
MONGO_URI=your_db_uri
JWT_SECRET=your_secret
GOOGLE_GENAI_API_KEY=your_key
```

Run:

```bash
npm run dev
```

---

### Frontend

```bash
cd Frontend
npm install
npm run dev
```

---

## 📡 API Overview

- POST /api/auth/... → authentication
- POST /api/interview/analyze → resume + JD analysis
- GET /api/interview/result/:id → fetch results

---

## 🧠 Key Learning Outcomes

- Designing AI-powered backend systems
- Prompt engineering for structured outputs
- Handling AI hallucination control
- Integrating GenAI into real-world workflows
- Building end-to-end full-stack applications

---

## 🚧 Future Improvements

- Real-time mock interview (chat-based)
- Voice-based interview simulation
- Resume auto-optimization for ATS
- Better scoring algorithm (ML-based)
