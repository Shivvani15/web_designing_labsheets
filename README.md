# Web Design Lab Work (MCA108P)

A collection of all my **Web Design** lab sheet solutions, starting from basic HTML and CSS, moving through JavaScript, and ending with full-stack PHP/MySQL and Python web applications.

| | |
|---|---|
| **Name** | Shivani |
| **Roll No.** | CU26280050 |
| **Course** | MCA – Web Design (MCA108P) |

---

## Tech Stack

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D22128?logo=apache&logoColor=white)

---

## Repository Structure

| Lab Sheet | Topic | Tech | Questions |
|-----------|-------|------|-----------|
| [LabSheet1](./LabSheet1) | HTML fundamentals: headings, text, lists, links, images, tables | HTML | Q1 – Q25 |
| [LabSheet2](./LabSheet2) | Forms, form controls and CSS styling | HTML, CSS | Q1 – Q22 |
| [LabSheet3](./LabSheet3) | JavaScript: DOM, events, closures, ES6, JSON, callbacks, mini apps (calculator, to-do list, slider, clock) | JavaScript | Q1 – Q21 |
| [LabSheet4](./LabSheet4) | PHP and MySQL with PDO: CRUD, sessions, cookies, file upload, transactions, password hashing, Apache config | PHP, MySQL | Q1 – Q21 |
| [LabSheet5](./LabSheet5) | Python web programming: CGI/WSGI, MySQL connector, SQLAlchemy ORM, connection pooling, JSON endpoints, backups | Python, MySQL | Q1 – Q21 |
| [LabSheet6](./LabSheet6) | Python web programming (revised copy of Lab Sheet 5 programs) | Python, MySQL | Q1 – Q21 |
| [LabSheet7](./LabSheet7) | Online **Bookstore** application: cart, checkout, orders, reviews, wishlist, admin panel, sales report | PHP, MySQL, JS | Q1 – Q21 |
| [LabSheet8](./LabSheet8) | Responsive multi-page **Portfolio Website**: dark/light mode, modal, FAQ accordion, carousel, form validation | HTML, CSS, JS | Q1 – Q19 |
| [LabSheet9](./LabSheet9) | **PHP and MySQL web app**: auth, product CRUD, pagination, search, image upload, shopping cart, SQLi and XSS demos | PHP, MySQL | Q1 – Q20 |
| [LabSheet10](./LabSheet10) | **MVC PHP project** (no framework): router, REST API, CSRF protection, secure sessions, PHPMailer, HTTPS and virtual host | PHP, MySQL, Apache | Q1 – Q20 |

Lab Sheets 7 to 10 contain their own `README.md` or `QUESTION_MAP.md` that maps every question to the file that solves it.

---

## Getting Started

### Clone the repository

```bash
git clone https://github.com/Shivvani15/Shivani_WebDesign_CU26280050.git
cd Shivani_WebDesign_CU26280050
```

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge)
- [XAMPP](https://www.apachefriends.org/) / WAMP / LAMP with **PHP 8+** and **MySQL** (Lab Sheets 4, 7, 9, 10)
- **Python 3.10+** (Lab Sheets 5, 6)
- [Composer](https://getcomposer.org/) (Lab Sheet 10 only, for PHPMailer)

---

## How to Run Each Lab Sheet

### Lab Sheets 1, 2, 3 and 8: static pages
No setup needed. Open any `.html` file in your browser (for Lab Sheet 8, open `index.html`).

### Lab Sheet 4: PHP + PDO
1. Copy the `LabSheet4` folder into `htdocs` (XAMPP) or `www` (WAMP).
2. Start Apache and MySQL.
3. Import `sql/setup.sql` (creates the `college_db` database).
4. Check credentials in `config/db.php`.
5. Open `http://localhost/LabSheet4/<question-folder>/` in the browser.

### Lab Sheets 5 and 6: Python
```bash
cd LabSheet5
pip install -r requirements.txt
mysql -u root -p < sql/setup.sql        # creates python_web_db
python q03_db_version/db_version.py     # run any question script
```
Database settings live in `common/db_config.py`. CGI scripts need Apache with CGI/WSGI enabled (see `q01`, `q10`, `q20`).

### Lab Sheet 7: Bookstore
1. Copy `LabSheet7` into `htdocs`.
2. Import `database.sql` (creates `bookstore_db`) and update `config.php`.
3. Open `http://localhost/LabSheet7/`.
4. See `QUESTION_MAP.md` for the full testing checklist.

### Lab Sheet 9: PHP and MySQL web app
1. Copy `LabSheet9` into `htdocs`.
2. Import `database.sql` (creates `webapp_db`) and check `config/db.php`.
3. Make sure `uploads/` is writable.
4. Open `http://localhost/LabSheet9/`, register an account and log in.

### Lab Sheet 10: MVC project
```bash
cd LabSheet10
composer install
mysql -u root -p < database/schema.sql
mysql -u root -p < database/mysql_user.sql
```
Then configure the Apache virtual host and SSL as described in `docs/SETUP_GUIDE.md` and open `https://myproject.local`.
Secrets are read from environment variables (`DB_HOST`, `DB_NAME`, `DB_USER`, `DB_PASS`, `SMTP_*`, `APP_URL`).

---

## Key Concepts Covered

- Semantic HTML5, forms and responsive layouts with Flexbox and Grid
- DOM manipulation, events, closures, ES6 features and `fetch()` API calls
- CRUD operations with PDO, `mysqli` and SQLAlchemy
- Authentication with sessions, cookies, "Remember Me" and `password_hash()`
- Security: prepared statements, CSRF tokens, XSS prevention, secure file uploads, least-privilege database users
- MVC architecture, front controller routing and REST APIs with token authentication
- Apache configuration: virtual hosts, `.htaccess`, SSL/TLS, access logs

---

## Notes

- Several programs use default local credentials (`root` with no password). **Change them before deploying anywhere public.**
- `LabSheet9/sqli_demo.php` is intentionally vulnerable and exists for demonstration only. Do not deploy it.
- These projects are for educational purposes and are not production ready.

---

## Author

**Shivani** (CU26280050)
MCA, Web Design Lab
