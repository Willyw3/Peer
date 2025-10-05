# 🎓 Peer — AI-Powered Micro-Expression Analysis for Student Engagement  

---

## 📖 Overview  
**Peer** is an **AI-powered micro-expression analyzer** designed to help educators measure **student engagement and comprehension** in real-time virtual classrooms.  

In an age where online learning is the norm, teachers can no longer read the subtle body language or expressions that indicate confusion or disengagement. Peer bridges this gap — analyzing live video feeds to identify when students are lost, distracted, or fully engaged, and automatically generating actionable feedback for instructors and learners.  

---

## 💡 Inspiration  
During online classes, educators lose access to the most powerful form of feedback — *facial and emotional cues*. When a student looks confused in-person, a teacher can re-explain immediately. But over Google Meet or Zoom, that signal is lost.  

We were inspired to create an **intelligent, real-time system** that restores this ability through AI — helping teachers understand when students are struggling and ensuring no one falls behind.  

---

## 🧠 What It Does  

**Peer** performs **real-time facial expression analysis** on classroom video feeds to detect:  
- 🟢 **Engaged** students (focused, attentive expressions)  
- 🟡 **Confused** students (raised eyebrows, squinting, head tilts)  
- 🔴 **Disengaged** students (looking away, eye closure, frowning)  

Once detected, Peer:  
1. **Scores engagement** for each student in real-time  
2. **Sends automated emails** — personalized feedback for students, summary reports for instructors  
3. **Stores analytics** — detailed engagement metrics in a **Supabase** database  
4. **Visualizes data** — through a live **React dashboard** for instructors  

---

## 🧩 Key Features  
✅ **Real-Time Facial Analysis** – Uses **OpenCV**, **MediaPipe Face Mesh**, and **DeepFace** to detect micro-expressions with 468 facial landmarks.  
✅ **Emotion Detection** – Powered by **RetinaFace**, **MTCNN**, and **YOLO-Face** models for multi-face environments.  
✅ **Engagement Scoring** – Custom heuristics combine facial landmarks + emotion probabilities to classify confusion, disengagement, or focus.  
✅ **Intelligent Automation** – **Mastra Agents** orchestrate AI workflows, integrating Supabase and Gmail for end-to-end processing.  
✅ **Email Reports** – Personalized feedback for students, instructor summaries with engagement insights, and improvement tips.  
✅ **Secure & Scalable** – Built with **Supabase** for authentication, storage, and real-time updates.  

---

## 🏗️ How We Built It  

**Computer Vision & Emotion Recognition**  
- **OpenCV** — for real-time video frame processing  
- **MediaPipe Face Mesh** — 468 facial landmarks for precise expression tracking  
- **DeepFace** — emotion classification using multiple backends (RetinaFace, MTCNN, YOLO-Face)  

**AI & Workflow Orchestration**  
- **Mastra Framework (TypeScript)** — agent-based architecture orchestrating workflows and LLM prompts  
- **Google Gemini 1.5 Pro** — contextual reasoning and content generation for personalized feedback  

**Database & API**  
- **Supabase** — authentication, data persistence, and live updates of session analytics  
- **FastAPI** — handles API routing, webhook management, and coordination with the Mastra agents  

**Email Automation**  
- **Nodemailer (Gmail SMTP)** — sends personalized HTML summaries to students and instructors  

**Frontend**  
- **React (Next.js)** — instructor dashboard for visualizing engagement heatmaps and per-student analytics  

---

## ⚙️ Tech Stack  

| Category | Tools / Frameworks |
|-----------|--------------------|
| **Frontend** | React, Next.js, TailwindCSS |
| **Backend** | FastAPI, TypeScript (Mastra Framework) |
| **AI / ML** | OpenCV, MediaPipe, DeepFace, RetinaFace, MTCNN, YOLO-Face |
| **Agents** | Mastra AI Agents, Google Gemini 1.5 Pro |
| **Database** | Supabase |
| **Automation** | Nodemailer (Gmail SMTP) |
| **Cloud / APIs** | Google Cloud, OAuth 2.0 |
| **Video Ingestion** | Recall.ai for Google Meet recordings |

---

## 🧱 System Architecture  
<img width="303" height="608" alt="image" src="https://github.com/user-attachments/assets/69741a1c-42e6-48e9-a39f-f6fda2f7547c" />
