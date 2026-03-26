# Vault Times 

Vault Times is a role-based news publishing platform built with **Django** and **Django REST Framework**.
It allows publishers, editors, journalists, and readers to interact with articles and newsletters through a structured workflow.

---

## Features

* Role-based access system:

  * **Reader** → view articles/newsletters
  * **Journalist** → create articles/newsletters
  * **Editor** → approve, update, and delete content
  * **Publisher** → manage teams and content
* Article approval workflow
* Newsletter creation system
* Publisher dashboard with linked users
* RESTful API with authentication & permissions
* Automated unit tests for all roles

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/giavassallo/vault-times
cd vault-times/news_project
```

---

### 2. Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Apply Migrations

```bash
python manage.py migrate
```

---

### 5. Run the Server

```bash
python manage.py runserver
```

Visit:

```
http://127.0.0.1:8000/
```

---

## Admin Setup

Create an admin user:

```bash
python manage.py createsuperuser
```

Then go to:

```
http://127.0.0.1:8000/admin/
```

---

## Running Tests

```bash
python manage.py test
```

Tests include:

* Role-based access validation
* Article approval logic
* API endpoint behavior
* Subscription filtering

---

## API Endpoints

| Method | Endpoint                    | Description                 |
| ------ | --------------------------- | --------------------------- |
| GET    | `/api/articles/`            | All approved articles       |
| GET    | `/api/articles/subscribed/` | Subscribed content          |
| GET    | `/api/articles/<id>/`       | Single article              |
| POST   | `/api/articles/`            | Create article (journalist) |
| PUT    | `/api/articles/<id>/`       | Update article              |
| DELETE | `/api/articles/<id>/`       | Delete article              |

---

## Documentation (Sphinx)

To view generated documentation:

Open:

```
docs/build/html/index.html
```

---

## Docker Setup

Build and run the container:

```bash
docker build -t vault-times .
docker run -p 8000:8000 vault-times
```

---

## Project Structure

```
vault-times/
│── api/
│── docs/
│── templates/
│── static/
│── manage.py
│── requirements.txt
│── Dockerfile
```

---

## Notes

* Do **not** commit `venv/` or sensitive data
* Ensure migrations are applied before running
* API permissions are strictly role-based

---

## Capstone Submission

Repository Link:
https://github.com/giavassallo/vault-times

---

## Author

giavassallo
