# 📦 Project Recommender Agent

An intelligent project recommender system built with **Django**, **FastAPI**, and **Vue.js**. This tool helps users discover personalized coding project ideas based on their tech stack, preferred project type, and difficulty level.

---

## 🔧 Tech Stack

- **Backend**: Django (with SQLite or PostgreSQL)
- **Recommendation Engine**: FastAPI (microservice)
- **Frontend**: Vue.js
- **Database**: Django ORM with JSONField for flexible tech stack storage

---

## 🚀 Features

- Store and manage project ideas using Django
- Recommend projects based on tech stack, type, and difficulty
- Interactive frontend to get real-time suggestions (coming soon)
- Modular architecture with FastAPI microservice for ML logic

---

## 📁 Project Structure

```bash
project-recommender-agent/
├── backend/           # Django backend (project + app)
│   └── projects/      # Django app for project ideas
├── recommender_api/   # FastAPI microservice for recommendations
├── frontend/          # Vue.js frontend (TBD)
├── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/project-recommender-agent.git
cd project-recommender-agent
```

### 2. Setup Django Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

📌 Create sample data (optional):

```bash
python manage.py shell
```

```python
from projects.models import ProjectIdea
ProjectIdea.objects.create(name="Django Project Tracker", stack=["Django", "PostgreSQL"], type="web app", difficulty="intermediate")
```

### 3. Setup FastAPI Microservice

```bash
cd ../recommender_api
pip install fastapi uvicorn django-environ
uvicorn main:app --reload
```

🧠 `main.py` will connect to Django DB and serve recommendations (we’ll build this in Step 2).

---

## 🛠️ To Do

- [x] Set up Django backend + project model
- [ ] Build FastAPI recommender service
- [ ] Connect Vue frontend to FastAPI
- [ ] Deploy full stack (Render/Vercel/etc.)

---

## 📄 License

MIT License. Free to use and modify.

---

## ✨ Author

**Aby Thomas** – (https://github.com/thomasaby)
