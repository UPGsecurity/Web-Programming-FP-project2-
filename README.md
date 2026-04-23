# Web-Programming-FP-project2-
# 📚 Book Swap / Lending Library

A web application that allows users to share, borrow, and lend books within a community.  
Built with Django, this project satisfies all capstone requirements including authentication, ORM, session handling, custom error pages, and clean frontend/backend separation.

---

## ✨ Features

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

---

## 🧱 Project Structure
book_swap/
├── manage.py
├── requirements.txt
├── README.md
├── book_swap/ # project settings
│ ├── init.py
│ ├── settings.py
│ ├── urls.py
│ └── wsgi.py
├── apps/
│ ├── accounts/ # registration, login, profile
│ ├── books/ # book CRUD, listing, detail
│ ├── borrowing/ # borrow requests, approvals
│ └── reviews/ # ratings and comments
├── static/ # CSS, JS, images
└── templates/ # base.html, home.html, 404.html, 500.html
