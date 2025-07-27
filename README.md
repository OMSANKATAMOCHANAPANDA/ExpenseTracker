# 💰 Expense Tracker - JavaFX Application

![App Demo](https://placehold.co/1200x600/3a4a7a/white?text=Expense+Tracker+Demo)

A feature-rich personal finance manager with SQLite database, JavaFX UI, and analytics.

## 📌 Features

- **Expense Management**: Add/edit/delete transactions
- **Category System**: Customizable with budget limits
- **Visual Analytics**: Interactive charts (Pie/Bar)
- **CSV Export**: Save reports in spreadsheet format
- **Dark/Light Mode**: Choose your preferred theme

## 🛠 Tech Stack
Component

Technology

Language

Java 17 (LTS)

GUI Framework

JavaFX 17

Database

SQLite (Embedded)

Build Tool

Maven

Charts

JFreeChart

🚀 Quick Start
Prerequisites
Java JDK 17+
Maven 3.8+
bash

Run
Copy code
# 1. Clone repository
git clone https://github.com/yourusername/expense-tracker.git
cd expense-tracker

# 2. Build & Run
mvn clean javafx:run

# Alternative: Run from JAR
mvn package
java -jar target/expense-tracker-1.0-jar-with-dependencies.jar
🖥️ UI Screens
Dashboard

Expenses

Categories

Dashboard

Expenses

Categories

🗄 Database Schema
![Schema Diagram](https://placehold.co/800x500/2a4365/white?text=Database+Schema%0A%0ATables%3A%0A- categories%0A- expenses)

sql

Run
Copy code
CREATE TABLE categories (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT UNIQUE NOT NULL,
    budget_limit REAL DEFAULT 0.0
);

CREATE TABLE expenses (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    amount REAL NOT NULL,
    category_id INTEGER NOT NULL,
    date TEXT NOT NULL,
    description TEXT,
    FOREIGN KEY (category_id) REFERENCES categories(id)
);
📂 Project Structure

Run
Copy code
expense-tracker/
├── src/main/java/com/expensetracker/
│   ├── controllers/       # JavaFX Controllers
│   ├── models/            # Data Models
│   ├── database/          # SQLite operations
│   └── utils/             # Helper classes
├── src/main/resources/    # FXML/CSS files
├── data/                  # SQLite database
└── target/                # Compiled output
🧪 Testing
bash

Run
Copy code
# Run all tests
mvn test

# Generate coverage report
mvn jacoco:report
Coverage Report:

Models: 100%
DAOs: 85%
Controllers: 75%
🔧 Configuration
Edit src/main/resources/config.properties:

properties

Run
Copy code
# SQLite Config
db.url=jdbc:sqlite:data/expenses.db

# UI Settings
ui.theme=dark
date.format=MM/dd/yyyy
🤝 How to Contribute
Fork the project
Create a feature branch (git checkout -b feature/amazing-feature)
Commit changes (git commit -m 'Add feature')
Push (git push origin feature/amazing-feature)
Open Pull Request
📜 License
MIT Om Sankata Mochana Panda


