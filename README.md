# 🗓️ Smart AI Calendar Scheduler

A Python-based command-line smart scheduling assistant that helps you manage your Google Calendar more effectively. It lets you **reorganize events by priority and due date**, **intelligently fit tasks into free time**, and even **generate AI-powered summaries** of your schedule using Google Gemini.

![calendar visualization](https://upload.wikimedia.org/wikipedia/commons/2/24/Google_Calendar_icon_%282020%29.svg)

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

### 🔧 Custom Event Metadata
- Uses event descriptions to track:
  - `Movable: True/False`
  - `Due Date: YYYY-MM-DD`
- Uses **color codes** to assign priority:
  - 🔴 `ASAP` → Color ID 11
  - 🟠 `High` → Color ID 5
  - 🟡 `Average` → Color ID 7
  - 🔵 `Low` → Color ID 10

---

## 🧑‍💻 Skills Demonstrated

- **Google Calendar API integration**
- **AI content generation using Gemini**
- **Algorithmic time-slot optimization**
- **Datetime and timezone manipulation with `pytz`**
- **CLI-based user experience design**
- Modular and maintainable **Python scripting**

---

## 🛠️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/smart-calendar-scheduler.git
cd smart-calendar-scheduler
