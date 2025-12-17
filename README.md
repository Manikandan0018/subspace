SubSpace – Clueso.io Clone

A full-stack clone of Clueso.io built as part of the SubSpace technical assignment.
This project focuses on screen recording, video processing, AI-powered transcription, and interactive playback, demonstrating end-to-end system design and execution.

🔗 Live Demo: https://subspace-seven.vercel.app/

📂 GitHub Repository: https://github.com/Manikandan0018/subspace

🧠 Product Overview

SubSpace enables users to:

Authenticate securely

Upload or record screen videos via a browser extension

Process videos using AI (speech-to-text & summarization)

View outputs with an interactive video player, transcript, and timeline controls

The product mirrors Clueso’s core workflows and UX patterns, prioritizing functionality and system integration over pixel-perfect design.

✨ Core Features
🔐 Authentication

Email-based signup & login

JWT-based session management

Protected routes

📊 Dashboard

Central hub for managing video productions

Upload video or record screen via extension

🎥 Video Processing

Video upload & storage

Audio extraction from video

AI-powered speech-to-text using Deepgram

Section detection & summaries using Gemini

🧩 Browser Extension

Screen & audio recording

Sends recording directly to backend

Seamless integration with web app

▶️ Player & Insights

Video playback

Interactive timeline bar (section-based navigation)

Full transcript synced with video

Section-wise navigation

🏗️ System Architecture
High-level Flow
User → Auth → Dashboard
     → Upload / Screen Record (Extension)
     → Backend Processing
     → Deepgram (STT) + Gemini (AI)
     → Player (Video + Transcript + Timeline)

Components

Frontend: React + Vite + Tailwind CSS

Backend: Node.js + Express + Socket.IO

AI Services: Deepgram (STT), Gemini (Summarization)

Extension: Chrome Extension (screen recording)

📁 Repository Structure
subspace/
├── frontend/        # React + UI (Vite)
├── backend/         # Node.js APIs + AI pipeline
├── extension/       # Browser extension (screen recording)
├── README.md
└── .gitignore

🛠️ Tech Stack

Frontend

React (Vite)

Tailwind CSS

GSAP (animations)

Socket.IO Client

Axios

Backend

Node.js

Express

Socket.IO

JWT Authentication

FFmpeg (video/audio processing)

AI

Deepgram (Speech-to-Text)

Gemini API (Summaries & insights)

Deployment

Frontend: Vercel

Backend: Render

⚙️ Local Setup Instructions
1️⃣ Clone Repository
git clone https://github.com/Manikandan0018/subspace.git
cd subspace

2️⃣ Frontend Setup
cd frontend
npm install
npm run dev


Create .env:

VITE_BACKEND_URL=http://localhost:5000

3️⃣ Backend Setup
cd backend
npm install
npm start


Create .env:

PORT=5000
JWT_SECRET=your_secret
DEEPGRAM_API_KEY=your_key
GEMINI_API_KEY=your_key

4️⃣ Extension Setup

Open Chrome → chrome://extensions

Enable Developer Mode

Click Load unpacked

Select the extension/ folder

🧪 Error Handling & Debugging

Backend uses try/catch at every critical step

Logs each stage of the video → AI pipeline

Socket status updates for real-time feedback

Graceful frontend loading & fallback states

📌 Design Decisions & Assumptions

Focused on feature parity over pixel perfection

Modular architecture for scalability

AI calls abstracted into service layers

Extension kept lightweight and isolated

Mock-friendly AI integration (can be swapped easily)

🎥 Demo Walkthrough

The demo video covers:

User onboarding & authentication

Dashboard usage

Video upload & screen recording

Backend processing flow

AI transcription & output

Player controls & timeline navigation

(Demo link provided during submission)

🚧 Limitations / Future Improvements

Advanced video editing tools

Team collaboration & comments

Analytics dashboard

Export formats (PDF, Docs)

Real-time collaborative playback

👤 Author

Manikandan
MERN Stack Developer
GitHub: https://github.com/Manikandan0018
