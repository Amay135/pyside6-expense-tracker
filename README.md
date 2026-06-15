# ExpenseTracker - Трекер расходов 
Трекер расходов написанный на Python с использованием фреймворка PySide6 с хранением записей в БД SQLite

![Screenshot 2023-05-01 203531](https://user-images.githubusercontent.com/26361250/235498237-62d36f89-6f75-4d78-bc83-8dd0ab8b166f.jpg)

# Expense Tracker (PySide6)

A desktop expense tracking application built using PySide6 and SQLite. The application helps users manage personal finances by recording income and expenses, organizing transactions into categories, and displaying financial summaries through a modern graphical user interface.

## Features

- Add new transactions
- Edit existing transactions
- Delete transactions
- Store transaction data using SQLite
- Automatically calculate total balance
- Track total income and outcome
- View expense totals by category
- User-friendly Qt GUI
- Automatic database creation

## Categories

The application supports the following categories:

- Work
- Auto
- Grocery
- Entertainment
- Other

## Technologies Used

- Python 3
- PySide6
- SQLite
- Qt Designer

## Project Structure

```text
expense-tracker/
│
├── main.py
├── connection.py
├── ui_main.py
├── new_transaction.py
├── new_transaction.ui
├── res.py
├── res-rs.qrc
├── expense_db.db
└── icons/
```

## Database Schema

Table: `expenses`

| Column | Type |
|----------|----------|
| ID | INTEGER PRIMARY KEY AUTOINCREMENT |
| Date | VARCHAR(20) |
| Category | VARCHAR(20) |
| Description | VARCHAR(20) |
| Balance | REAL |
| Status | VARCHAR(20) |

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/pyside6-expense-tracker.git
cd pyside6-expense-tracker
```

### Create Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate virtual environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install PySide6
```

## Running the Application

```bash
python main.py
```

## How to Use

### Add Transaction

1. Click **New Transaction**
2. Select a category
3. Choose a date
4. Enter a description
5. Enter the balance amount
6. Select Income or Outcome
7. Click **Save Transaction**

### Edit Transaction

1. Select a transaction from the table
2. Click **Edit Transaction**
3. Modify the data
4. Save the changes

### Delete Transaction

1. Select a transaction
2. Click **Delete Transaction**
3. The transaction will be removed from the database

## Dashboard Summary

The application automatically calculates:

- Current Balance
- Total Income
- Total Outcome
- Grocery Expenses
- Auto Expenses
- Entertainment Expenses
- Other Expenses

## Main Components

### connection.py

Handles:

- SQLite database connection
- Table creation
- Insert operations
- Update operations
- Delete operations
- Financial calculations

### main.py

Handles:

- Main application window
- Loading transaction data
- User interactions
- Connecting buttons and events
- Opening transaction dialogs

### new_transaction.py

Contains the PySide6 UI generated from Qt Designer for creating and editing transactions.

### ui_main.py

Contains the main dashboard UI generated from Qt Designer.

### res.py

Compiled Qt resource file containing SVG icons used throughout the application.

## Screenshots

### Main Dashboard

Features:

- Current balance display
- Income and outcome summaries
- Expense category statistics
- Transaction history table

### Transaction Dialog

Features:

- Category selection
- Date selection
- Description input
- Balance input
- Status selection
- Save transaction button

## Future Improvements

- Transaction search
- Date filtering
- Export to Excel
- Export to PDF
- Monthly reports
- Charts and analytics
- Dark mode support
- User authentication
- Multi-user support

## Repository Information

**Repository Name**

```text
pyside6-expense-tracker
```

**Description**

```text
A desktop expense tracker application built with PySide6 and SQLite for managing personal finances, tracking income and expenses, and viewing financial summaries.
```

**Topics**

```text
python
pyside6
qt
sqlite
desktop-application
expense-tracker
finance-manager
personal-finance
gui
qt-designer
```

## First Commit

```bash
git add .
git commit -m "Initial commit: Expense Tracker application using PySide6 and SQLite"
git branch -M main
git remote add origin https://github.com/USERNAME/pyside6-expense-tracker.git
git push -u origin main
```

## License

This project is intended for educational purposes and personal use.
