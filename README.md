# Career Conversations AI Agent 🤖

An AI-powered conversational assistant that represents my professional profile and acts as a personal portfolio chatbot. It answers questions about my background, skills, and experience while also logging user interest and unknown queries using tool-calling.

---

## Features

- Conversational AI chatbot powered by Google Gemini (OpenAI-compatible API)
- Context-aware responses using LinkedIn PDF + personal summary
- Tool-calling system:
  - Records user emails, names, and notes
  - Logs unknown or unanswered questions
- Built using Gradio for a simple web interface
- Optional notification system using Pushover API

---

## 📁 Project Structure

career_conversations/
│
├── app.py — Main chatbot application
├── linkedin.pdf — Resume exported from LinkedIn
├── summary.txt — Personal summary text
├── me/
│   ├── linkedin.pdf — LinkedIn PDF used by the model
│   └── summary.txt — Summary used by the model
└── .gradio/ — Temporary system files (ignored in Git)

---

## How It Works

- The app loads your LinkedIn PDF and summary text
- These are injected into the system prompt
- Users interact through a Gradio chat interface
- The model:
  - Responds as your professional persona
  - Uses tools when needed:
    - record_user_details → stores interested users
    - record_unknown_question → logs unanswered queries
- Optional push notifications are sent via Pushover API

---

## Tech Stack

- Python
- Google Gemini API (via OpenAI SDK compatibility layer)
- Gradio
- PyPDF
- Requests
- python-dotenv

---

## Environment Variables

Create a .env file with:

GOOGLE_API_KEY=your_google_gemini_api_key  
PUSHOVER_TOKEN=your_pushover_token  
PUSHOVER_USER=your_pushover_user_key  

---

## Run Locally

pip install -r requirements.txt  
python app.py  

Then open:

http://127.0.0.1:7860

---

## Example Use Cases

- Personal AI portfolio chatbot
- Recruiter interaction assistant
- Automated lead capture system
- Interactive resume experience

---

## Notes

- .gradio/ is auto-generated and should not be pushed to GitHub
- Ensure files exist inside me/ before running the project
- Requires a model that supports function/tool calling

---

## Author

Shriya Yadavalli  
Personal AI career assistant project

---

## Project Structure Overview

career_conversations/
│
├── app.py Main chatbot application
├── linkedin.pdf Resume exported from LinkedIn
├── summary.txt Personal summary text
├── me/
│ ├── linkedin.pdf LinkedIn PDF used by model
│ └── summary.txt Summary used by model
└── .gradio/ Temporary system files (ignored in git)
