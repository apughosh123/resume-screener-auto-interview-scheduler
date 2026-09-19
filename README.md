# Resume Screener + Auto Interview Scheduler

An AI-powered recruitment automation system built with **n8n**, **OpenRouter**, **Gmail**, and **Google Calendar + Google Meet**.

This project automates the recruitment process from **resume submission and AI screening to interview scheduling and confirmation**.

---

## 🚀 Project Overview

This project consists of two n8n workflows that automate the candidate screening and interview scheduling process.

### Workflow 1 — Resume Screener + Auto Interview Scheduler

Candidates submit their resume through an n8n form. The workflow extracts the resume text, analyzes it using AI, and determines whether the candidate is shortlisted.

If the candidate is shortlisted, an automated interview invitation email is sent with a link to the interview scheduling form.

### Workflow 2 — Interview Scheduler

The shortlisted candidate submits their preferred interview date and time through the scheduling form.

The workflow then automatically:

* Creates a Google Calendar event
* Generates a Google Meet link
* Sends an interview confirmation email to the candidate

---

## 🔄 Workflow Architecture

### Workflow 1 — Resume Screener + Auto Interview Scheduler

```text
Resume Submission Form
        ↓
Extract Resume Text
        ↓
AI Resume Screening
        ↓
Parse AI Screening Result
        ↓
Shortlisted?
        ↓ TRUE
Interview Invitation Email
        ↓
Interview Scheduling Form
```

### Workflow 2 — Interview Scheduler

```text
Interview Scheduling Form
        ↓
Create Google Calendar Event
        ↓
Generate Google Meet
        ↓
Interview Confirmation Email
```

---

## ✨ Features

* 📄 Resume submission through an n8n form
* 📑 PDF resume text extraction
* 🤖 AI-powered resume screening
* 🎯 Candidate match score from 0–100
* ✅ Automatic shortlist decision
* 📧 Automated interview invitation
* 📅 Interview date and time collection
* 🗓️ Automatic Google Calendar event creation
* 🎥 Automatic Google Meet generation
* 📩 Automated interview confirmation
* 🔄 End-to-end recruitment automation

---

## 🛠️ Technologies Used

| Technology      | Purpose                         |
| --------------- | ------------------------------- |
| n8n             | Workflow automation             |
| OpenRouter      | AI API integration              |
| OpenAI GPT-5.2  | Resume analysis                 |
| Gmail           | Automated email communication   |
| Google Calendar | Interview scheduling            |
| Google Meet     | Online interview                |
| JavaScript      | Data parsing and transformation |

---

## 📂 Project Files

```text
├── README.md
├── 01 Resume Screener.json
└── 02 Interview Scheduler.json
```

### 01 Resume Screener.json

This workflow handles:

* Candidate resume submission
* Resume PDF text extraction
* AI resume screening
* Match score generation
* Shortlist decision
* Automated interview invitation

### 02 Interview Sch
