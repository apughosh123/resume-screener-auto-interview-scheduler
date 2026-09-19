# Resume Screener + Auto Interview Scheduler

An AI-powered recruitment automation system built with **n8n, OpenRouter, Gmail, Google Calendar, and Google Meet**.

This project automates the recruitment workflow from **resume submission and AI screening to interview scheduling and confirmation**.

---

## 🚀 Project Overview

The system consists of two connected n8n workflows.

### Workflow 1 — Resume Screener + Auto Interview Scheduler

Candidates submit their resume through an n8n form.

The workflow:

* Extracts text from the uploaded PDF resume
* Analyzes the resume using AI
* Generates a candidate match score
* Determines whether the candidate is shortlisted
* Sends an interview invitation email to shortlisted candidates

### Workflow 2 — Interview Scheduler

Shortlisted candidates use the scheduling form to provide their preferred interview date and time.

The workflow then:

* Creates a Google Calendar event
* Automatically generates a Google Meet link
* Sends an interview confirmation email

---

## 🔄 End-to-End Workflow

```text
Candidate
   ↓
Resume Submission Form
   ↓
PDF Resume Extraction
   ↓
AI Resume Screening
   ↓
Parse Screening Result
   ↓
Shortlisted?
   ├── TRUE → Interview Invitation Email
   │              ↓
   │      Interview Scheduling Form
   │              ↓
   │      Google Calendar Event
   │              ↓
   │        Google Meet Link
   │              ↓
   │      Confirmation Email
   │
   └── FALSE → Workflow Ends
```

---

## 🧩 Workflow 1 — Resume Screener + Auto Interview Scheduler

```text
On Form Submission
        ↓
Extract from File
        ↓
OpenRouter AI Resume Screener
        ↓
Parse AI Screening Result
        ↓
Shortlisted?
        ↓ TRUE
Send Interview Invitation
```

### AI Screening Output

The AI evaluates the candidate against the applied job position and returns structured JSON data.

Example:

```json
{
  "candidate_name": "Candidate Name",
  "email": "candidate@example.com",
  "job_position": "AI Automation Engineer",
  "match_score": 78,
  "shortlisted": true,
  "skills": [],
  "experience_summary": "",
  "education": "",
  "strengths": [],
  "missing_requirements": [],
  "reason": ""
}
```

The `shortlisted` value controls whether the candidate receives an interview invitation.

---

## 📅 Workflow 2 — Interview Scheduler

```text
Interview Scheduling Form
        ↓
Google Calendar Event
        ↓
Google Meet Generation
        ↓
Interview Confirmation Email
```

The workflow collects:

* Candidate Name
* Email
* Interview Date
* Interview Time

It then creates a scheduled calendar event with a Google Meet link and sends the details to the candidate automatically.

---

## ✨ Key Features

* 📄 Resume submission through n8n Form
* 📑 PDF resume text extraction
* 🤖 AI-powered resume screening
* 🎯 Match score generation from 0–100
* ✅ Automated shortlist decision
* 📧 Automated interview invitation
* 📝 Interview scheduling form
* 🗓️ Google Calendar integration
* 🎥 Automatic Google Meet generation
* 📩 Interview confirmation email
* 🔄 End-to-end recruitment automation

---

## 🛠️ Technologies Used

| Technology          | Purpose                         |
| ------------------- | ------------------------------- |
| **n8n**             | Workflow automation             |
| **OpenRouter**      | AI API integration              |
| **OpenAI GPT-5.2**  | Resume analysis                 |
| **Gmail**           | Automated email communication   |
| **Google Calendar** | Interview scheduling            |
| **Google Meet**     | Online interviews               |
| **JavaScript**      | Data parsing and transformation |

---

## 📂 Project Structure

```text
resume-screener-auto-interview-scheduler/
│
├── README.md
├── 01-resume-screener.json
├── 02-interview-scheduler.json
│
├── interview 1.png
├── interview 2.png
├── interview mail.png
└── interview confirmed.png
```

---

## 📸 Workflow Screenshots

### Workflow 1 — Resume Screener

![Resume Screener Workflow](interview%201.png)

### Workflow 2 — Interview Scheduler

![Interview Scheduler Workflow](interview%202.png)

---

## 📧 Interview Invitation

After successful AI screening and shortlisting, the candidate automatically receives an interview invitation email containing the scheduling form.

![Interview Invitation Email](interview%20mail.png)

---

## ✅ Interview Confirmation

After the candidate submits their preferred interview date and time, the system creates the calendar event and sends a confirmation email containing the interview details and Google Meet link.

![Interview Confirmation Email](interview%20confirmed.png)

---

## 🧪 End-to-End Testing

The complete recruitment automation was tested successfully.

| Step                       | Status       |
| -------------------------- | ------------ |
| Resume submission          | ✅ Successful |
| PDF text extraction        | ✅ Successful |
| AI resume screening        | ✅ Successful |
| Match score generation     | ✅ Successful |
| Shortlist decision         | ✅ Successful |
| Interview invitation       | ✅ Successful |
| Scheduling form submission | ✅ Successful |
| Google Calendar event      | ✅ Successful |
| Google Meet generation     | ✅ Successful |
| Confirmation email         | ✅ Successful |

---

## 🎯 Use Cases

This automation can be adapted for:

* Recruitment agencies
* HR departments
* Startups
* Internship hiring
* Remote recruitment
* Freelance recruiters
* Automated candidate screening
* Interview scheduling

---

## 🔮 Future Improvements

Potential improvements include:

* Automated rejection emails
* Candidate database integration
* Google Sheets / database storage
* Interview reminders
* Automatic calendar availability checking
* Advanced job-resume matching
* Recruitment analytics dashboard
* ATS / CRM integration

---

## 🔐 Security

Sensitive credentials should never be committed to GitHub.

This project uses external credentials for API and Google services. Credentials should be configured securely inside n8n using credentials or environment variables.

**Never commit API keys, OAuth tokens, passwords, or other secrets to the repository.**

---

## 👨‍💻 Author

### Apu Ghosh

**AI Automation Specialist**

Focused on:

* n8n Workflow Automation
* AI Agents
* API Integrations
* Business Process Automation
* AI-powered Recruitment Automation

---

## ⭐ Project Goal

The goal of this project is to demonstrate how **AI and workflow automation** can streamline the recruitment process by connecting resume screening, candidate communication, interview scheduling, Google Calendar, and Google Meet into one automated system.
