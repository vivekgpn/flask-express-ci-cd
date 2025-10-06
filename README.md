# Flask & Express CI/CD Deployment Assignment

## 1. Project Overview
This project deploys:
- **Backend:** Flask application running on Python 3.12
- **Frontend:** Express application running on Node.js
- **CI/CD:** Automated deployment using Jenkins

Both applications are hosted on a single AWS EC2 instance.

---

## 2. Architecture
         +----------------------+
         |      EC2 Instance    |
         |----------------------|
         | Flask Backend: 5000 |
         | Express Frontend: 3000|
         +----------------------+
                 |
           Public IP: 3.110.164.231

---

## 3. Deployment Steps

### Backend (Flask)
```bash
cd ~/flask-express-ci-cd/backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
export FLASK_APP=app.py
export FLASK_ENV=production
flask run --host=0.0.0.0 --port=5000 &
