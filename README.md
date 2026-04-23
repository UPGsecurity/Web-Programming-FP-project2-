📚 Book Swap / Lending Library

A web application that allows users to share, borrow, and lend books within a community.
Built with Django, this project satisfies all capstone requirements including authentication,
ORM, session handling, custom error pages, and clean frontend/backend separation.

✨ Features

- User registration, login, logout (with remember‑me via session)
- Each user has a profile (phone, address, karma score)
- Add, edit, delete books (title, author, genre, condition)
- Browse all available books with search and filter
- Send borrow requests to book owners
- Approve / reject / mark as returned for incoming requests
- Rate and review borrowed books
- Admin panel to manage users, books, and requests
- Custom 404 and 500 error pages
- Fully responsive HTML/CSS with JavaScript enhancements

🧱 Project Structure

book_swap/
├── manage.py
├── requirements.txt
├── README.md
├── book_swap/               # project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── accounts/            # registration, login, profile
│   ├── books/               # book CRUD, listing, detail
│   ├── borrowing/           # borrow requests, approvals
│   └── reviews/             # ratings and comments
├── static/                  # CSS, JS, images
└── templates/               # base.html, home.html, 404.html, 500.html

Each app directory contains its own README.md describing its purpose.

📦 Requirements

- Python 3.10 or higher
- Django 4.2+
- SQLite (default) or PostgreSQL
- crispy‑forms (optional)

All dependencies are listed in requirements.txt.

🚀 Installation & Setup

1. Clone the repository
   git clone https://github.com/your-team/book-swap.git
   cd book-swap

2. Create a virtual environment
   python -m venv venv
   source venv/bin/activate      # Linux/Mac
   venv\Scripts\activate         # Windows

3. Install dependencies
   pip install -r requirements.txt

4. Apply migrations
   python manage.py makemigrations
   python manage.py migrate

5. Create a superuser (admin)
   python manage.py createsuperuser

6. Run the development server
   python manage.py runserver

7. Open http://127.0.0.1:8000 in your browser.

🔧 Configuration

- Set DEBUG = True in settings.py for development.
- For production, set DEBUG = False and configure ALLOWED_HOSTS and static file serving.
- Session is stored in database (default) – no extra setup required.

👥 Team Collaboration

This project is designed for 4 team members, each responsible for one Django app:

| Member | App          | Responsibilities                                      |
|--------|--------------|-------------------------------------------------------|
| A      | accounts     | User registration, login, logout, profile management |
| B      | books        | Add/Edit/Delete books, list/detail views, search      |
| C      | borrowing    | Borrow requests, approval, return tracking           |
| D      | reviews      | Star ratings, comments, JavaScript + CSS styling     |

All apps are developed independently and later integrated into a single Django project via urls.py.

📄 Functionality Checklist (for grading)

URL routing & Django templates     -> Each app has its own urls.py; views use render() with HTML templates.
Authentication & admin panel       -> django.contrib.auth + custom UserProfile; admin can manage all models.
Database ORM & custom models       -> Book, BorrowRequest, UserProfile, Review models with relationships.
Custom error pages                 -> templates/404.html, 500.html and handlers in urls.py.
Session & user data handling       -> request.user everywhere; login required; session cookie keeps user logged in.
HTML / CSS                         -> Responsive design in static/css/style.css with consistent navbar.
JavaScript                         -> Live search, AJAX borrow request, dynamic status updates.
Django                             -> Core framework used throughout.
React / DRF (optional)             -> Not mandatory – can be added later.
README.md per directory            -> Every app folder contains a short README.md.
Clean code (no LLM clutter)        -> Simple, well‑commented without auto‑generated boilerplate.
GitHub contribution                -> Each team member commits regularly; final submission is main branch.

🧪 Testing (manual)

- Register a new user → verify profile is created.
- Login → add a book.
- Another user registers → searches for the book → sends a borrow request.
- Original owner logs in → approves request.
- Borrower marks book as returned → owner can rate the borrower.
- Try accessing protected pages while logged out → redirect to login.
- Visit a non‑existent URL → custom 404 page.

📸 Screenshots (to be added)

Add screenshots of home page, book list, borrow request form, and admin panel here.

📚 License

This project is developed for educational purposes (SE201 – Web Programming).
No external license applied – use only within the course context.

🙌 Acknowledgements

- Django documentation
- Bootstrap (if used)
- FontAwesome for icons (optional)
