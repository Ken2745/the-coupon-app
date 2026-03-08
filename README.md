# The Coupon App Prototype

The Coupon App is a safety-focused mobile platform disguised as a coupon application to discreetly provide access to safety resources and incident logging. A multi-component repository combining an Android client, a Django API server, and a minimal web interface.

---

## Core Components

| Directory | Purpose | Notes |
|-----------|---------|-------|
| `app/` | **Android mobile application** | Java/Gradle project with UI, services, and ML models. See [app/README.md](app/README.md). |
| `backend/` | **Django backend & API** | Data storage, handles auth, and exposes REST endpoints. See [backend/README.md](backend/README.md). |
| `frontend/` | **Web templates & static assets** | Simple Django templates that use HTMX to call the API. See [frontend/README.md](frontend/README.md). |


---
## Tech Stack

Backend
- Python
- Django
- Django REST Framework
- JWT Authentication

Mobile
- Android (Java)
- Gradle
- TensorFlow Lite
- Porcupine Wake Word Detection

Frontend
- Django Templates
- HTMX

---

### Backend

```bash
cd backend
python -m venv venv
venv\Scripts\activate          # Windows
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

API lives at `http://127.0.0.1:8000/api/`; admin at `/admin/`.

### Android Client

Open `app/` in Android Studio or:

```bash
cd c:\Users\kensh\the-coupon-app
gradlew assembleDebug
```

Configure the base URL (e.g. `http://10.0.2.2:8000/api/` for emulator) then install/run on a device.

### Web UI

No build step. Visit `http://127.0.0.1:8000/` after starting the backend. Templates fetch data with HTMX.

---

## Architecture Overview

Android App
      │
      │ REST API
      ▼
Django Backend
      │
      ▼
Database

## Architecture Highlights

* **Discreet UI** – the mobile app appears as a coupon app, with safe‑exit and hidden PIN navigation.
* **Voice & ML** – uses Porcupine wake words and TensorFlow Lite models stored in `app/src/main/assets/`.
* **REST API** – JWT authentication via `rest_framework_simplejwt`; endpoints managed with DRF viewsets and generic views.
* **Small web frontend** – basic login/register pages and dynamic incident log fetching.

---

## Collaboration

This project was developed collaboratively. Team members contributed across frontend development, backend services, database design, AI integration, and CI/CD setup.
Implemented user stories in Jira to mitigate development risks and organize tasks, actively leveraging Scrum meetings to drive application progress.

<img width="365" height="848" alt="image" src="https://github.com/user-attachments/assets/6dc76a84-2886-4b3e-90b1-cc2b1d3faa7b" />
<img width="365" height="839" alt="image" src="https://github.com/user-attachments/assets/2acf89a6-308b-4ba2-b9f2-feaaa2acad1d" />
<img width="377" height="850" alt="image" src="https://github.com/user-attachments/assets/c6c932c1-29c9-44cb-9857-22c840f57c72" />
<img width="377" height="850" alt="image" src="https://github.com/user-attachments/assets/eb2ec87c-6ef8-49db-bdee-af2cdabca224" />
<img width="365" height="750" alt="image" src="https://github.com/user-attachments/assets/5772f61c-c225-403c-8286-161ba68da184" />
<img width="365" height="750" alt="image" src="https://github.com/user-attachments/assets/c5f3b892-e544-4f8a-b941-52111d2cb88c" />
<img width="371" height="762" alt="image" src="https://github.com/user-attachments/assets/b581f61a-a6e4-493c-836a-0d8caf51ea03" />
<img width="366" height="752" alt="image" src="https://github.com/user-attachments/assets/c6d0a24b-e83c-4744-b2ae-0c0373f247e6" />
<img width="365" height="750" alt="image" src="https://github.com/user-attachments/assets/b6c2fdb1-df64-47d3-801e-188f75641454" />
<img width="365" height="750" alt="image" src="https://github.com/user-attachments/assets/af677b1f-830a-4276-b152-8460bb1eef22" />
<img width="371" height="762" alt="image" src="https://github.com/user-attachments/assets/abca73ed-9be2-4c22-a340-063a98c8b088" />
<img width="366" height="752" alt="image" src="https://github.com/user-attachments/assets/17ba5684-17ba-4fab-b52e-c28de93f9669" />









