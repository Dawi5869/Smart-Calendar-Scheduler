# 🗓️ Smart AI Calendar Scheduler

A Python-based command-line smart scheduling assistant that helps you manage your Google Calendar more effectively. It lets you **reorganize events by priority and due date**, **intelligently fit tasks into free time**, and even **generate AI-powered summaries** of your schedule using Google Gemini.

![calendar visualization](![image](https://github.com/user-attachments/assets/97afd800-a7c7-46f6-afc7-43964edbd358))

---

## 🚀 Features

### ✅ Event Management
- **Add and organize events**: Add tasks with estimated time, due date, and priority. The script finds optimal time slots for each.
- **Reorganize existing events**: Based on deadline and priority, events are rescheduled to maximize productivity.

### 🤖 AI Integration
- **Gemini-powered schedule summaries**: Get helpful summaries based on your calendar data and custom prompts (e.g., "What’s my workload like tomorrow?").

### 🧠 Smart Scheduling Logic
- Differentiates between **movable** and **fixed** events.
- Respects your working hours (10:30 AM – 10:00 PM).
- Automatically avoids early mornings, late nights, and overlapping time blocks.
- Provides a 15-minute buffer time between events.

### 🔧 Custom Event Metadata
- Uses event descriptions to track:
  - `Movable: True/False`
  - `Due Date: YYYY-MM-DD`
- Uses **color codes** to assign priority:
  - 🔴 `ASAP` → Color ID 11
  - 🟡 `High` → Color ID 5
  - 🔵 `Average` → Color ID 7
  - 🟢 `Low` → Color ID 10

---

## 🧑‍💻 Skills Demonstrated

- **Google Calendar API integration**
- **Gemini API integration**
- **AI content generation using Gemini**
- **Algorithmic time-slot optimization**
- **Datetime and timezone manipulation with `pytz`**
- **CLI-based user experience design**
- Modular and maintainable **Python scripting**

---

## 📡 API Integrations

This project integrates two powerful APIs:

### 1. **Google Calendar API**
- **Purpose:** Authenticates the user, reads calendar events, and programmatically adds, updates, or reorganizes them.
- **Usage Highlights:**
  - Retrieves upcoming events from the user's primary calendar.
  - Inserts or patches events based on available time slots.
  - Uses OAuth 2.0 authentication flow via `credentials.json` and `token.json`.

### 2. **Google Gemini API**
- **Purpose:** Generates intelligent summaries of the user's schedule using natural language prompts.
- **Usage Highlights:**
  - Converts structured calendar data into plain-text summaries.
  - Accepts custom user prompts like: *"What's my day looking like?"* or *"Which days are the busiest this week?"*
  - Integrates with `gemini-2.0-flash-001` model via the `google.genai` SDK.

These integrations demonstrate the blend of automation, personalization, and AI-powered insights within a real productivity workflow.

