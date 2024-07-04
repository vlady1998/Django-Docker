# Introduction

This repository provides an easy way to initiate a Django project using Docker. It comes with pre-configured services including PostgreSQL, Redis, Celery (worker and beat), Nginx, and Traefik, ready to run a Django web application. Additionally, it provides a few handy shortcuts for easier development.

# Technical Details
- **Django** web application framework
- **PostgreSQL** database
- **Redis** in-memory data structure store
- **Celery** worker and beat services for running background tasks asynchronously
- **Nginx** web server for serving static and media files, and proxying requests to the Django application
- **Traefik** reverse proxy for routing requests to the appropriate service and providing SSL termination

## Included Packages and Tools

- **Pytest**: Testing framework
- **Pytest Sugar**: A pytest plugin for a better look
- **Pytest Django**: A pytest plugin providing useful tools for testing Django applications
- **Coverage**: Test coverage tool
- **Ruff**: Linter
- **Black**: Code formatter

# How to run the project

1. Clone repository with ```git clone https://github.com/godd0t/django-docker-quickstart.git```.

2. Change directory into the project: ```cd django-docker-quickstart```.

3. Copy the `env.example` file to `.env` and update the values as needed.

4. Create a virtual environment:
    ```bash
    python -m venv venv
    ```

5. Activate the virtual environment:
    ```bash
    source venv/bin/activate
    ```

6. Install the development requirements specific to your IDE for enhanced functionality and support(Optional).
    ```bash
    pip install -r src/requirements.dev.txt
    ```
7. Run the server.
    - Use Docker compose
    ```bash
     docker-compose -f docker-compose.yml up --build -d
    ```
    - use Make for shortcut
    ```bash
     make build-dev
    ```
   

## Shortcut

This project includes several shortcuts to streamline the development process:

- **Create migrations:**
    ```bash
    make make-migrations
    ```

- **Run migrations:**
    ```bash
    make migrate
    ```

- **Run the linter:**
    ```bash
    make lint
    ```

- **Run the formatter:**
    ```bash
    make format
    ```

- **Run the tests:**
    ```bash
    make test
    ```

- **Create a super user:**
    ```bash
    make super-user
    ```

- **Build and run dev environment:**
    ```bash
    make build-dev
    ```

- **Build and run prod environment:**
    ```bash
    make build-prod
    ```
---
