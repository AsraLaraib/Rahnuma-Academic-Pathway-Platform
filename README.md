# Rahnuma: Academic Pathway Platform

> *Your intelligent compass for navigating post-matric and intermediate academic transitions in Pakistan.*

---

## 🚀 Project Overview

**Rahnuma** is a full-stack, eligibility-aware academic guidance web application designed to help Pakistani students navigate the critical transition points after completing their Matric (Secondary School Certificate) or Intermediate (Higher Secondary School Certificate) studies. 

Instead of acting as a generic, ungrounded career chatbot, Rahnuma combines a strict **deterministic eligibility engine** with multi-criteria preference matching. It evaluates a student's verified academic profile against real-world prerequisite rules sourced from official educational guidelines (such as BISE and HEC policies) and presents side-by-side comparative pathway analyses with clear, audit-ready justifications.

---

## ✨ Key Features

* **Deterministic Eligibility Filtering:** Automatically screens out unviable academic tracks based on hard prerequisites (e.g., mandatory subjects, minimum passing scores) to prevent false positives and rule violations.
* **Weighted Multi-Criteria Scoring:** Ranks eligible pathways transparently using a balanced algorithm considering academic alignment, individual subject strengths, and practical constraints (e.g., location, budget).
* **Side-by-Side Comparison Matrix:** Empowers students to compare 2–3 pathways simultaneously, contrasting requirements, career prospects, and trade-offs.
* **Grounded AI Explanations:** Utilizes a lightweight LLM acting strictly on structured JSON rule outputs to translate technical match results into empathetic, plain-English guidance without hallucinations.
* **Source-Backed Audit Trails:** Every recommendation includes clear citations of the governing bodies, policy documents, and verification years.
* **Secure Student Profiles:** Allows students to save their assessment reports securely and track their educational options.

---

## 🛠️ Tech Stack

Rahnuma is built on a robust, modern full-stack architecture:

* **Frontend:** React.js (Vite), Tailwind CSS (responsive user interfaces, multi-step assessment forms).
* **Backend:** Node.js, Express.js (RESTful APIs, server-side business logic execution).
* **Database & ORM:** PostgreSQL / MongoDB with structured relational schemas for tracking students, marks, pathways, and rules.
* **Validation:** Zod (strict runtime validation for student marks and form inputs).
* **AI Layer:** Lightweight LLM API (integrated via secure backend endpoints for natural language explanations).
* **Testing:** Jest / Supertest for backend and logic verification.

---

## 🏗️ System Architecture & Workflow

1. **Profile Ingestion & Normalization:** Converts raw obtained and total marks into accurate percentage metrics and subject-wise competencies.
2. **Hard Rule Enforcement:** The Node.js backend evaluates hard constraints (e.g., *Pre-Engineering requires Intermediate Mathematics*). Unqualified paths are immediately filtered out.
3. **Soft Scoring:** Eligible pathways are scored using weighted parameters for interests and strengths.
4. **Natural Language Translation:** The structured results JSON is passed to the AI module to generate clean, accessible student reports.

---

## 📂 Repository Structure

```text
rahnuma-platform/
├── frontend/             # React.js (Vite) client application
│   ├── src/
│   │   ├── components/   # Reusable UI components & forms
│   │   ├── pages/        # Assessment, Results, and Comparison views
│   │   └── App.jsx
│   └── package.json
├── backend/              # Node.js & Express.js server
│   ├── controllers/      # Business logic & eligibility engine
│   ├── models/           # Database schemas
│   ├── routes/           # API endpoints
│   └── server.js
└── README.md
