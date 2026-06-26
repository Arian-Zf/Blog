<div align="center">

<h1>📝 Blog — Django Web Application</h1>

<p>
  A full-featured blog platform built with Django, featuring a clean UI, post management, image support, and a custom CSS design system.
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-Framework-092E20?style=for-the-badge&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS-Custom%20Design-264de4?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
</p>

<p>
  <a href="#-features">Features</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-screenshots">Screenshots</a> •
  <a href="#-contributing">Contributing</a>
</p>

</div>

---

## ✨ Features

- 📄 **Post Management** — Create, edit, and publish blog posts with rich content
- 🖼️ **Image Support** — Upload and display images within posts via `images/post_images/`
- 🎨 **Custom Styling** — Hand-crafted CSS design system located in `static/css/`
- 🔧 **Django Admin Panel** — Full control over content through Django's built-in admin interface
- 🧩 **Modular Architecture** — Separated `blog` app and `sabzweb` project config for clean organization
- ⚡ **Lightweight & Fast** — No heavy frontend frameworks, just clean HTML/CSS/JS

---

## 📁 Project Structure

```
Blog/
│
├── blog/                   # Main blog application
│   ├── migrations/         # Database migrations
│   ├── templates/          # HTML templates for blog views
│   ├── admin.py            # Admin panel configuration
│   ├── models.py           # Post, Category, and other data models
│   ├── views.py            # View logic for handling requests
│   └── urls.py             # URL routing for blog endpoints
│
├── sabzweb/                # Django project configuration
│   ├── settings.py         # Project settings (DB, apps, static files, etc.)
│   ├── urls.py             # Root URL configuration
│   └── wsgi.py             # WSGI entry point for deployment
│
├── static/
│   └── css/                # Custom stylesheets
│
├── images/
│   └── post_images/        # Uploaded post images
│
├── manage.py               # Django management command entry point
└── .gitignore
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.8+
- pip
- Git

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/Arian-Zf/Blog.git
cd Blog
```

**2. Create and activate a virtual environment**

```bash
# On Linux / macOS
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate
```

**3. Install dependencies**

```bash
pip install django pillow
```

> If a `requirements.txt` is available:
> ```bash
> pip install -r requirements.txt
> ```

**4. Apply database migrations**

```bash
python manage.py migrate
```

**5. Create a superuser (for admin access)**

```bash
python manage.py createsuperuser
```

**6. Run the development server**

```bash
python manage.py runserver
```


---

## ⚙️ Configuration

The project settings are located in `sabzweb/settings.py`. Key settings you may want to customize:

| Setting | Description |
|--------|-------------|
| `DATABASES` | Database backend (default: SQLite) |
| `STATIC_URL` | URL for serving static files |
| `MEDIA_URL` / `MEDIA_ROOT` | URL and path for uploaded images |
| `ALLOWED_HOSTS` | Hosts allowed to serve the application |
| `SECRET_KEY` | Django secret key — **keep this private in production!** |

---

## 🌐 Deployment

For production deployment, consider the following steps:

1. Set `DEBUG = False` in `settings.py`
2. Update `ALLOWED_HOSTS` with your domain
3. Use a production-grade database (PostgreSQL recommended)
4. Serve static files via a web server (Nginx / Apache) or a CDN
5. Use **Gunicorn** or **uWSGI** as the WSGI server

```bash
# Example with Gunicorn
pip install gunicorn
gunicorn sabzweb.wsgi:application
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Python 3** | Core language |
| **Django** | Web framework (MVC pattern) |
| **SQLite** | Development database |
| **HTML5** | Template structure |
| **CSS3** | Custom styling & layout |
| **JavaScript** | Frontend interactivity |
| **Pillow** | Image upload & processing |

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. Fork this repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add: your feature description"`
4. Push to your fork: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please make sure your code follows the existing style and includes relevant comments where needed.

---

## 📋 Roadmap

- [ ] Add user authentication (register / login)
- [ ] Add comment system for posts
- [ ] Implement post categories and tags
- [ ] Add pagination for post listings
- [ ] Add search functionality
- [ ] REST API support with Django REST Framework
- [ ] Responsive mobile layout improvements

---

## 📄 License

This project is open source. Feel free to use, modify, and distribute it.

---

<div align="center">

Made with ❤️ by [Arian-Zf](https://github.com/Arian-Zf)

⭐ If you found this project useful, consider giving it a star!

</div>