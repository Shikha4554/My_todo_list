# My_todo_list

A simple ToDo list web app built with Flask. Add, edit, and delete tasks stored in a SQLite database through a Bootstrap-styled interface.

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Heroku](https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white)

## Features

- Add a task with a title and description from the home page
- View all tasks in a list
- Edit a task's title/description via a dedicated update page
- Delete a task
- Data persisted with SQLAlchemy to a SQLite database (`todo.db`)
- Database schema managed with Flask-Migrate/Alembic (`migrations/`)
- Bootstrap 5 UI served through Jinja2 templates
- `Procfile` included for deployment to Heroku with Gunicorn

## Getting Started

### Prerequisites

- Python 3.x

### Installation

```bash
git clone https://github.com/Shikha4554/My_todo_list.git
cd My_todo_list
python -m venv env
source env/bin/activate     # On Windows: env\Scripts\activate
pip install -r requirements.txt
```

### Run locally

```bash
python app.py
```

The app creates `todo.db` automatically on first run and starts at `http://127.0.0.1:5000`.

If you make changes to the `Todo` model, generate and apply a migration with Flask-Migrate:

```bash
flask db migrate -m "description of change"
flask db upgrade
```

### Deployment

A `Procfile` (`web: gunicorn app:app`) is included for deploying to Heroku.

## Screenshots

![Screenshot 1](Screenshot_(105).png)
![Screenshot 2](Screenshot_(106).png)
