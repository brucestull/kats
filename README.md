# Kats 🐾

**Kats** is a Django skeleton project that integrates reusable "kat-themed" Django apps as external packages. It is designed to help you compose a cohesive application from separately maintained Django apps such as:

- [Kat Corner](https://github.com/brucestull/kats-kat-corner) – Manage kat records
- [Kat Food Corner](https://github.com/brucestull/kats-kat-food-corner) – Manage kat food and feeding
- [Kitten Corner](https://github.com/brucestull/kats-kitten-corner) – Manage younger kat records (kittens)

---

## 📦 Project Structure

This repository is the **host project**. It imports external Django apps via editable installs (`-e`) or compressed source distributions (`.tar.gz`).

The project follows this structure:

```
kats/
├── LICENSE
├── Pipfile         # Dependency management (Pipenv)
├── Pipfile.lock
├── README.md
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py     # Django project settings
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── notes
    ├── 00_commands_and_links.md        # Common commands and links
    └── chatgpt_project_creation.md     # Dev notes and ChatGPT instructions
```

---

## 🚀 Getting Started

### 🔧 Install Dependencies

Use [Pipenv](https://pipenv.pypa.io/en/latest/) to install dependencies:

```bash
pipenv install --dev
```

### 📦 Install Django Apps

#### Option 1: Editable mode (good for development)

```bash
pipenv install -e ../kats-kitten-corner/
pipenv install -e ../kats-kat-food-corner/
pipenv install -e ../kats-kat-corner/
```

#### Option 2: From built `.tar.gz` packages

```bash
pipenv install ../kats-kitten-corner/dist/KittenCorner-0.1.tar.gz
pipenv install ../kats-kat-food-corner/dist/KatFoodCorner-0.1.tar.gz
pipenv install ../kats-kat-corner/dist/KatCorner-0.1.tar.gz
```

---

## 🛠️ Common Commands

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser --email your@email.com --username youruser
python manage.py runserver
```

You may also need to run:

```bash
python manage.py makemigrations kitten_corner
python manage.py makemigrations kat_food_corner
```

---

## 🌐 App URLs

| App             | URL                                                              |
| --------------- | ---------------------------------------------------------------- |
| Admin           | [http://localhost:8000/admin/](http://localhost:8000/admin/)     |
| Kitten Corner   | [http://localhost:8000/kittens/](http://localhost:8000/kittens/) |
| Kat Food Corner | [http://localhost:8000/foods/](http://localhost:8000/foods/)     |
| Kat Corner      | [http://localhost:8000/kats/](http://localhost:8000/kats/)       |

---

## 🧪 Development Notes

* See [`notes/chatgpt_project_creation.md`](notes/chatgpt_project_creation.md) for ChatGPT-generated planning.
* See [`notes/00_commands_and_links.md`](notes/00_commands_and_links.md) for quick commands and links.

---

## 📜 License

[MIT License](LICENSE)

---

## ✨ Author

Created by [Flynnt Knapp](mailto:FlynntKnapp@gmail.com) — because life’s better with kats.
