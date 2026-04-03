1 Digimart Cedar - Reference Solution

This repository contains the clean, production-ready source code for the **Digimart Cedar** e-commerce platform. It serves as the reference implementation for all 10 assigned tasks.

2 Project Structure

This repository is structured to support independent verification of each task via Git branches.

reference-solutions/
├── .git/               # Contains 11 branches: main, task-1 ... task-10
├── src/
│   ├── backend/        # Django REST Framework API
│   │   ├── Dockerfile
│   │   ├── requirements.txt
│   │   ├── seed_public.py
│   │   └── ...
│   └── frontend/       # Svelte + Vite Client
│       ├── Dockerfile.ecs
│       ├── package.json
│       └── ...
├── docker-compose.yml  # Orchestration for Dev/Prod
└── README.md

3. Key Features Implemented
Task 1-2: Product Catalog, Global Search, and Filtering.
Task 3-4: User Authentication (JWT/Session), Role-Based Access Control (RBAC).
Task 5: Security Hardening & Vulnerability Mitigation (SQLi, XSS, IDOR).
Task 6-7: Shopping Cart, Guest Checkout, and Order Management.
Task 8: Async Email Notifications (Background Tasks).
Task 9: Review System with Validation.
Task 10: Recommendation Engine (Category-based & Collaborative Filtering).

4.Tech Stack

Backend: Python 3.13, Django 5.1, Django REST Framework.
Frontend: Svelte 4, Vite, Bootstrap 5.
Database: PostgreSQL (Production) / SQLite (Dev).
Deployment: Docker, ECS Fargate, Nginx.

5. How to Run
-  docker-compose up --build #using docker
   Frontend: http://localhost:5173
   Backend API: http://localhost:3000
   Health Check: http://localhost:3000/health/

- Local Development
cd src/backend (FrontEnd)
pip install -r requirements.txt
python manage.py migrate
python seed_public.py
python manage.py runserver 0.0.0.0:3000

cd src/frontend
npm install
npm run dev

