#  Django Notes App

A full-stack **Notes Management Application** built using **Django** and
containerized with **Docker**.\
This project supports REST APIs, environment-based configuration, and
production-ready deployment using **Nginx**, **Docker Compose**, and
**CI/CD (Jenkins)**.

------------------------------------------------------------------------------------

##  Features

-   Create, Read, Update, Delete (CRUD) notes
-   RESTful APIs using Django & Django REST Framework
-   Environment variable support using `.env`
-   Docker & Docker Compose setup
-   Nginx reverse proxy configuration
-   CI/CD pipeline using Jenkins
-   Production-ready structure

-----------------------------------------------------------------------------------

## Tech Stack

### Backend

-   Django
-   Django REST Framework
-   Python 3.x
-   SQLite (default DB)

### DevOps & Deployment

-   Docker
-   Docker Compose
-   Nginx
-   Jenkins
-   Gunicorn
-   Procfile (for deployment platforms)

------------------------------------------------------------------------

##  Project Structure

    django-notes-app/
    │
    ├── api/                # API logic (serializers, views, urls)
    ├── mynotes/            # Notes app
    ├── notesapp/           # Main Django project
    ├── nginx/              # Nginx configuration
    ├── staticfiles/        # Collected static files
    │
    ├── author/             # Metadata / author info
    ├── Ubuntu/             # OS-related configs/scripts
    │
    ├── .env                # Environment variables
    ├── .gitignore
    ├── Dockerfile
    ├── docker-compose.yaml
    ├── Jenkinsfile         # CI/CD pipeline
    ├── Procfile            # Production process file
    ├── requirements.txt
    ├── manage.py
    ├── db.sqlite3
    └── README.md

------------------------------------------------------------------------

## Installation & Setup

### 1 Clone the repository

``` bash
git clone https://github.com/ShivanHussain/django-notes-app.git
cd django-notes-app
```

------------------------------------------------------------------------

### 2 Environment Setup

Create a `.env` file in root directory:

``` env
DEBUG=True
SECRET_KEY=your_secret_key
ALLOWED_HOSTS=*
```

------------------------------------------------------------------------

### 3 Run using Docker (Recommended)

``` bash
docker-compose up --build
```

Application will be available at:\
`http://localhost:8000`

------------------------------------------------------------------------

### 4 Manual Setup (Without Docker)

``` bash
pip install -r requirements.txt
python manage.py migrate
python manage.py collectstatic
python manage.py runserver
```

---------------------------------------------------------------------------

##  API Endpoints (Sample)

  Method   Endpoint                    Description
  -------- --------------------------- ---------------
  GET      /api/notes/                 Get all notes
  POST     /api/notes/                 Create note
  PUT      /api/notes/`<id>`{=html}/   Update note
  DELETE   /api/notes/`<id>`{=html}/   Delete note

-----------------------------------------------------------------------------

## CI/CD

-   Jenkins pipeline configured via `Jenkinsfile`
-   Automated build & deployment supported
-   Docker-based CI workflow

------------------------------------------------------------------------------

##  Learning Outcomes

-   Django REST API development
-   Dockerized backend architecture
-   Nginx reverse proxy setup
-   Environment-based configuration
-   CI/CD pipeline integration
-   Production-level project structuring


