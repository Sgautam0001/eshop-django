# eshop-django 🛍️ (Django E-Commerce)

A Django-based e-commerce project with product listing, cart/checkout flow, and an admin panel for managing products, orders, and users.

> Repo: https://github.com/Sgautam0001/eshop-django

---


https://github.com/user-attachments/assets/06672501-d8bc-490c-afdd-235fb3e6c7d3




## ✨ Features
- Product catalog (categories, product details)
- Cart & checkout flow
- User authentication (login/register)
- Admin dashboard (manage products, orders, users)
- Media/uploads support (product images)

> Feature list may vary depending on the apps enabled in this project.

---

## 🧰 Tech Stack
- Python
- Django
- SQLite (default, can be switched to Postgres/MySQL)
- HTML/CSS/JS (Django templates)

---

## 📦 Project Structure (high level)
.
├── manage.py
├── requirements.txt
├── db.sqlite3
├── Eshop/ # Django project settings
├── store/ # Main app (products/cart/orders etc.)
├── uploads/ # Media/uploads (usually ignored in git)
└── README.md

yaml
Copy code

---

## ✅ Prerequisites
- Python 3.10+ (recommended)
- pip

Check:
```bash
python --version
pip --version
🚀 Setup & Run (Local)
1) Clone the repo
bash
Copy code
git clone https://github.com/Sgautam0001/eshop-django.git
cd eshop-django
2) Create & activate virtual environment
macOS/Linux

bash
Copy code
python3 -m venv .venv
source .venv/bin/activate
Windows (PowerShell)

powershell
Copy code
py -m venv .venv
.\.venv\Scripts\Activate.ps1
3) Install dependencies
bash
Copy code
pip install -r requirements.txt
4) Apply migrations
bash
Copy code
python manage.py makemigrations
python manage.py migrate
5) Create admin user (optional)
bash
Copy code
python manage.py createsuperuser
6) Run the server
bash
Copy code
python manage.py runserver
Open:

App: http://127.0.0.1:8000/

Admin: http://127.0.0.1:8000/admin/

🔐 Environment Variables (Optional)
If your project uses a .env file (recommended), create one in the root:

env
Copy code
DEBUG=True
SECRET_KEY=change-me
ALLOWED_HOSTS=127.0.0.1,localhost
If your project doesn’t use environment variables yet, you can keep values directly in Eshop/settings.py.

🖼️ Static & Media Files
Common dev setup:

STATIC_URL = "/static/"

MEDIA_URL = "/media/"

MEDIA_ROOT = BASE_DIR / "uploads" or BASE_DIR / "media"

Collect static (only needed for production):

bash
Copy code
python manage.py collectstatic
🧪 Running Tests (if available)
bash
Copy code
python manage.py test
🛠️ Useful Admin Commands
Create migrations:

bash
Copy code
python manage.py makemigrations
Apply migrations:

bash
Copy code
python manage.py migrate
Create superuser:

bash
Copy code
python manage.py createsuperuser
📌 Deployment Notes (Quick)
For production, you should:

set DEBUG=False

configure ALLOWED_HOSTS

use a production DB (PostgreSQL recommended)

serve static/media via Nginx or a cloud storage/CDN

