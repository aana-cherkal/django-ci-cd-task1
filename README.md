# Django CI/CD Pipeline with Docker and GitHub Actions

## Project Overview
This project demonstrates a **CI/CD pipeline** for a Django web application using **Docker** and **GitHub Actions**.  
The workflow automatically builds, tests, and deploys a Docker image to Docker Hub whenever code is pushed to the `main` branch.

---

## Tools & Technologies
- Python 3.11 / Django 5.2.5
- Docker
- GitHub & GitHub Actions
- Docker Hub

---

## Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/django-ci-cd-task.git
cd django-ci-cd-task
```

## 2. Local development (optional)
```bash
python -m venv env
env\Scripts\activate       # Windows
pip install -r requirements.txt
python manage.py runserver
```
### 3. Docker

**Build Docker image:**
```bash
docker build -t my-django-app .
docker run -p 8000:8000 my-django-app
```
Open http://127.0.0.1:8000 in your browser to see the app.

CI/CD Pipeline

Trigger: Push to main branch

Steps:

Checkout code

Set up Python

Install dependencies

Run Django tests

Docker login using GitHub Secrets

Build Docker image

Push Docker image to Docker Hub

Secrets Used:

DOCKER_USERNAME → Docker Hub username

DOCKER_PASSWORD → Docker Hub password / personal access token

Verification: Workflow runs successfully in GitHub Actions and pushes the Docker image to Docker Hub (<username>/my-django-app:latest).


Screenshots of docker hub img verification and folder sturcture presend in folder named screenshots/
