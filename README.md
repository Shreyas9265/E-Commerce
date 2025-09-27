# E‑Commerce Web Application (PHP + MySQL)

A classic full‑stack e‑commerce web app built with **PHP**, **MySQL**, **HTML**, and **CSS**, designed to run locally with **XAMPP**. It includes customer‑facing shopping flows and an admin panel for catalog and order management.

## ✨ Features
- Product catalog with categories and search
- User authentication (sign up / login / logout) and session management
- Shopping cart & checkout
- Order history and details
- Admin dashboard for products, inventory, and orders
- Responsive UI with custom CSS

## 🧰 Tech Stack
- **Frontend:** HTML, CSS
- **Backend:** PHP (procedural or modular)
- **Database:** MySQL (via XAMPP’s MariaDB)
- **Local runtime:** XAMPP (Apache + MySQL)

## 🗂️ Project Structure (example)
```
ecommerce/
├─ public/               # public web root (index.php, assets, css, js)
├─ src/                  # PHP code (controllers, models, helpers)
├─ views/                # templates / partials
├─ config/               # db.php, constants.php
├─ sql/                  # schema.sql, seed.sql (optional)
└─ README.md
```
> If your layout differs, update this README to match your folders.

## 🚀 Local Setup (XAMPP on Windows/Mac)
1. **Clone or copy project into XAMPP**  
   - Windows: move the project folder into `C:\xampp\htdocs\ecommerce`
   - Mac (MAMP/XAMPP): `/Applications/XAMPP/htdocs/ecommerce`

2. **Create the database**
   - Start **Apache** and **MySQL** in XAMPP Control Panel.
   - Open **phpMyAdmin** (http://localhost/phpmyadmin).
   - Create a database, e.g. `ecommerce_db`.
   - Import your schema: **sql/schema.sql** (or create tables manually if you don’t have a file).

3. **Configure DB connection**
   - Edit `config/db.php` (or your connection file) with:
     ```php
     <?php
     $host = "localhost";
     $db   = "ecommerce_db";
     $user = "root";
     $pass = ""; // default for XAMPP is empty
     $conn = new mysqli($host, $user, $pass, $db);
     if ($conn->connect_error) { die("DB Connection failed: " . $conn->connect_error); }
     ?>
     ```

4. **Run the app**
  
   - Log in / sign up, browse products, add to cart, checkout.

## 🔐 Environment & Security
- Do **not** commit secrets (use a `.env` or move credentials to a local, ignored file).
- Sanitize inputs and use prepared statements for all SQL queries.
- Regenerate sessions on login, set secure cookie flags in production.

## 🧪 Test Data (optional)
- Use `sql/seed.sql` to load demo products and a test admin user.

