# 🤖 AI Planner Agent for Intelligent Project Planning

> IBM AICTE AI Automation and Intelligent Solutions – 6-Week Summer Internship 2026

## 📌 Overview
This project implements **Planner Agent (Agent 1)** of an AI-powered Project Management System using **n8n** and **OpenAI**.
The workflow accepts a project description, retrieves available employees and their skills from Google Sheets, and uses an AI Agent to automatically generate milestones, tasks, assign suitable employees, and store the project plan in a planning sheet.
This eliminates manual project planning and provides an intelligent starting point for project execution.

## 🎯 Problem Statement
Project managers spend significant time manually:

- Understanding project requirements
- Breaking projects into milestones
- Creating detailed tasks
- Assigning employees
- Maintaining planning sheets

These repetitive tasks are time-consuming and susceptible to human error.

## 💡 Solution
This workflow automates project planning using an AI-powered Planner Agent.
The AI:
- Understands the project description
- Reads employee information from Google Sheets
- Identifies employee skills and roles
- Generates milestones and tasks
- Assigns appropriate employees
- Produces structured output
- Automatically updates the Planner Sheet

# ⚙ Workflow Architecture

```
Project Description
        │
        ▼
Chat Trigger
        │
        ▼
Read Employee Data
(Google Sheets)
        │
        ▼
Employee Formatter
        │
        ▼
AI Planner Agent
(OpenAI GPT)
        │
        ▼
Structured Output Parser
        │
        ▼
Split Tasks
        │
        ▼
Append Tasks to Google Sheet
```

---

# 🛠 Workflow Steps

## 1. Chat Trigger

Receives the project description from the user.

Example

```
Develop an Online Food Delivery Application.
```

## 2. Read Employee Details
Retrieves employee information from Google Sheets including:
- Employee Name
- Role
- Skills
- Experience

## 3. Employee Processing
Formats employee data into a structure suitable for AI processing.

## 4. AI Planner Agent
The AI analyzes:
- Project requirements
- Employee skills
- Team composition

It then generates:

- Milestones
- Tasks
- Suggested employee assignments
- Estimated priorities

## 5. Structured Output Parser
Converts the AI response into structured JSON for downstream automation.
Example
```json
{
  "milestone": "Frontend Development",
  "task": "Create Homepage",
  "assigned_to": "Alice",
  "priority": "High"
}
```

## 6. Split Output
Each generated task is separated into individual records.

## 7. Update Planner Sheet
Each task is automatically appended into Google Sheets for project tracking.

# 🧠 AI Components
### OpenAI Chat Model
Responsible for:

- Project understanding
- Task generation
- Team assignment
- Planning

### Structured Output Parser
Ensures the AI response follows a predictable JSON structure for automation.

# 🧩 Technologies Used
- n8n
- OpenAI GPT
- Google Sheets API
- AI Agent
- Structured Output Parser
- Workflow Automation


# 📂 Workflow Nodes

| Node | Purpose |
|------|----------|
| When Chat Message Received | Workflow Trigger |
| Get Row(s) in Sheet | Read Employee Database |
| Employees | Format Employee Information |
| AI Agent | Intelligent Project Planner |
| OpenAI Chat Model | Large Language Model |
| Structured Output Parser | Convert AI Output into JSON |
| Split Out | Split Generated Tasks |
| Append Row in Sheet | Save Planner Data |

# 📥 Sample Input

```
Develop an E-commerce Website with User Login, Product Catalog, Payment Gateway, and Admin Dashboard.
```

# 📤 Sample Output

| Milestone | Task | Assigned To | Priority |
|-----------|------|-------------|----------|
| Requirement Analysis | Gather Requirements | Business Analyst | High |
| UI Design | Design Homepage | UI Designer | High |
| Backend Development | Develop APIs | Backend Developer | High |
| Frontend Development | Build Product Page | Frontend Developer | Medium |


# 📈 Features

- AI-powered project planning
- Automatic milestone generation
- Employee skill matching
- Intelligent task assignment
- Google Sheets integration
- Structured JSON output
- Automated planner sheet updates

# 📚 Learning Outcomes
During this project I learned:
- AI Workflow Automation using n8n
- Agentic AI Concepts
- OpenAI Integration
- Structured Output Parsing
- Google Sheets Automation
- Intelligent Project Planning
- Workflow Orchestration


# 🚀 Future Enhancements
- Multi-Agent Collaboration
- Deadline Prediction
- Automatic Reminder Emails
- Slack/WhatsApp Notifications
- Risk Analysis
- Progress Tracking Dashboard
- Calendar Integration

## 👩‍💻 Author
**Stephy Ann Biju**

B.Tech Computer Science Engineering

IBM AICTE AI Automation and Intelligent Solutions Internship – 2026

