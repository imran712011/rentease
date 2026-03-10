# rentease
# 🏠 RentEase — Furniture & Appliance Rental Platform

A fully client-side, browser-based rental management platform built with **vanilla HTML, CSS, and JavaScript**. No backend, no frameworks, no build tools — just open and run.

---

## 📸 Overview

RentEase simulates a real-world furniture and appliance rental service with two separate portals — a **User Portal** and an **Admin Dashboard** — both sharing a live database stored in the browser's `localStorage`.

---

## ✨ Features

### 🏠 User Portal
- Browse available products (furniture, appliances, electronics)
- Create new rental orders with flexible tenures (3 / 6 / 12 months)
- View active and past rentals
- Raise maintenance requests for rented items
- Track delivery status in real time

### ⚙️ Admin Dashboard
- Manage users, products, rentals, maintenance, and deliveries
- Full CRUD operations across all entities
- Live KPI analytics and reports
- View and update delivery agent assignments
- Monitor maintenance ticket priorities and statuses

### 🗄️ Shared Live Database
- Both portals read and write to the **same `localStorage` database**
- Changes in one portal are instantly reflected in the other
- One-click **Reset** to restore clean sample data at any time

---

## 🗂️ Project Structure

```
rentease/
├── index.html      # Landing page — launch pad for both portals
├── user.html       # User-facing portal
├── admin.html      # Admin dashboard
└── README.md
```

> ⚠️ All three HTML files **must be in the same folder** to work correctly.

---

## 🚀 Getting Started

### Option 1 — Run Locally (Simplest)
1. Clone or download this repository
2. Make sure `index.html`, `user.html`, and `admin.html` are in the **same folder**
3. Double-click `index.html` to open it in your browser
4. Click either portal button to get started

```bash
git clone https://github.com/YOUR_USERNAME/rentease.git
cd rentease
# Open index.html in your browser
```

### Option 2 — Serve via Live Server (Recommended for development)
If you have VS Code, install the **Live Server** extension and click "Go Live".

Or use Python's built-in server:
```bash
# Python 3
python -m http.server 8080
# Then open http://localhost:8080
```

---

## 🔐 Demo Credentials

| Portal | Email | Password |
|--------|-------|----------|
| User Portal | `imran@example.com` | `pass123` |
| Admin Dashboard | `admin@rentease.com` | `admin123` |

---

## 📊 Sample Database

The app seeds the following data automatically on first load:

| Entity | Count |
|--------|-------|
| Users | 5 |
| Products | 12 |
| Rentals | 7 |
| Maintenance Requests | 4 |
| Deliveries | 7 |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, CSS Grid, Flexbox) |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts — Playfair Display, DM Sans |

> **No frameworks. No dependencies. No build step.** Just open and run.

---

## 📦 Data Model

```
users        → id, name, email, phone, city, status, totalRentals
products     → id, name, category, rent, deposit, tenures, stock
rentals      → id, userId, productId, tenure, startDate, endDate, status
maintenance  → id, rentalId, userId, issue, priority, status
deliveries   → id, rentalId, type (delivery/pickup), scheduledDate, agent
```

---

## 🔄 Resetting the Database

Click the **"🔄 Reset Database to Sample Data"** button on the landing page (`index.html`) at any time to wipe all changes and restore the original seed data.

---

## 📁 Deploying to GitHub Pages

1. Push all three files to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your app will be live at:  
   `https://YOUR_USERNAME.github.io/REPO_NAME/`

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

Built with ❤️ using plain HTML, CSS & JS — no frameworks needed.
