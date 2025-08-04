# 💸 SpendSnap — A Python Budget Tracker App

![Python](https://img.shields.io/badge/Python-3.11+-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![MIT License](https://img.shields.io/badge/License-MIT-green)


**SpendSnap** is a simple and effective command-line budget tracker built in Python with MySQL integration. It helps you monitor monthly expenses by category, validate budgets, and prevent overspending.

---

## 🚀 Features

- 👤 **User Authentication**: Secure login and signup with per-user data isolation.
- 💰 **Monthly Budget Tracking**: Prompts for new budget every 30 days.
- 📊 **Categorized Expenses**: Track expenses in categories like Grocery, Entertainment, etc.
- 🧠 **Input Validation**: Ensures correct categories, dates, and safe amounts.
- 🧾 **Transaction History**: View all transactions or grouped summaries by category.
- ⚠️ **Over-Budget Warnings**: Alerts user before saving if a transaction will exceed budget.
- 🧹 **Edit/Delete Support**: Modify past transactions if needed.
- 📤 **CSV Export**: Export data for external analysis (if implemented).
  
---

## 🛠️ Tech Stack

- **Python 3.11+**
- **MySQL** (Connector: `mysql-connector-python`)
- Tables used: `user`, `transactions`, `remaining_budget`

---

## 📁 File Structure

project-root/
│
├── Budget Tracker app.py # Main runner file
├── Commands.py # Logic functions (add, edit, show, etc.)
├── README.md # Project description
└── requirements.txt # Python dependencies (if created)

---

## 🧪 How to Run

1. **Clone the repo**:
   git clone https://github.com/yourusername/spendsnap.git
   cd spendsnap

## 🧱 MySQL Setup Instructions

Create a database named spendsnap

Add required tables (see below)

Install dependencies:

    pip install mysql-connector-python
Run the app:

python "Budget Tracker app.py"
🗃️ MySQL Table Schema

CREATE TABLE user (
    username VARCHAR(100) PRIMARY KEY,
    password VARCHAR(100) NOT NULL
);

CREATE TABLE remaining_budget (
    username VARCHAR(100),
    initial_budget INT,
    amt_left INT,
    last_updated DATE,
    budget_start DATE
);

CREATE TABLE transactions (
    amount INT,
    date DATE,
    category VARCHAR(100),
    username VARCHAR(100)
);
⚠️ Known Limitations
No password encryption (stored as plain text).

No GUI (CLI-based).

No concurrency control for simultaneous users.

🧠 Future Improvements
Add Flask web frontend or Tkinter GUI

Add budget analytics dashboards

Improve CSV export interface

Support recurring expenses and future budget predictions

👤 Author
Made with ☕ and late-night debugging by Kaustubh (@kaustubh-x-d)
Feel free to fork, improve, or suggest ideas!

📄 License
MIT License — use, modify, and build upon this project freely.

---
