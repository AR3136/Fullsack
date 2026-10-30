# Dealerships Review Application

## Project Details
- **Project Name:** Dealerships Review Application
- **Repository Name:** Fullsack
- **GitHub Repository:** [https://github.com/AR3136/Fullsack](https://github.com/AR3136/Fullsack)
- **Author:** Abhay Amit Rajankar (AR3136)

---

## Project Overview
The **Dealerships Review Application** is a full-stack cloud application developed as part of the IBM Full Stack Cloud Developer Capstone Project. The application provides a comprehensive platform for managing car dealerships across the United States, allowing prospective car buyers and visitors to explore dealerships, view vehicle inventory, read dealership reviews with AI sentiment analysis, and submit their own reviews.

---

## Architecture & Tech Stack
- **Frontend:** HTML5, CSS3, JavaScript, React.js, Bootstrap
- **Backend / Web Framework:** Python (Django)
- **Microservices / Cloud Functions:** Node.js, Express, IBM Code Engine / Cloud Functions
- **Database:** SQLite (local Django data), MongoDB / IBM Cloudant (dealer and review data)
- **AI / Sentiment Analysis:** IBM Watson Natural Language Understanding (NLU)
- **DevOps & CI/CD:** GitHub Actions, Docker, Cloud Deployment

---

## Project Breakdown

### Prework: IBM Cloud & Watson NLU
1. IBM Cloud configuration and Watson Natural Language Understanding (NLU) service integration for sentiment analysis on reviews.

### Static Pages & Frontend
1. Forked repository and local workspace setup.
2. Responsive static pages: **About Us** (`server/frontend/static/About.html`) and **Contact Us** (`server/frontend/static/Contact.html`).
3. User registration and authentication pages built with React (`Register.jsx`, `Login.jsx`).

### Backend Microservices & Database
1. Node.js Express server to interface with MongoDB/Cloudant for dealer listings and customer reviews.
2. Cloud functions to query dealerships, fetch dealers by ID and state (e.g., Kansas), and retrieve reviews.
3. Microservice for sentiment analysis on review content using Watson NLU.

### Django Web Application
1. Django user management and session handling (login, logout, registration).
2. Django models for Car Make and Car Model with admin panel management.
3. Proxy services connecting the Django frontend to backend microservices for dealership information and review posting.

### Containerization & CI/CD
1. Dockerized Django application and backend services.
2. Continuous Integration and Continuous Deployment (CI/CD) pipeline configured with GitHub Actions.
3. Application deployment and cloud hosting.

---

## Setup & Running Locally

### 1. Clone the repository
```bash
git clone https://github.com/AR3136/Fullsack.git
cd Fullsack
```

### 2. Django Server Setup
```bash
cd server
python -m venv venv
# Windows
.\venv\Scripts\activate
# Linux/macOS
source venv/bin/activate

pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

---

## License
Distributed under the Apache 2.0 License. See `LICENSE` for more information.
