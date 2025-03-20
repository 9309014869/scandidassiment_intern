# 📌 Import Transactions in MySQL & Dashboard UI

## 🚀 Overview
This project consists of a **Java backend** to import transactions from **Excel to MySQL**, a **Node.js API server**, and a **React.js frontend** to visualize and filter transaction data.

## 🏗 Tech Stack
- **Frontend**: React.js, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **Data Processing**: Java (Excel to CSV & MySQL Connectivity)
- **Libraries**: MySQL Connector (Java), Axios, React Router, Express
🛠 Technologies Used

Language: Java (JDBC for database connection)

Database: MySQL

Libraries: JDBC, MySQL Connector
📂 Database Schema

1. Category Table

2. Product Table

3. Transactions Table

📌 Steps to Run the Java Import Process

Install MySQL and create the database.

Update database credentials in the Java application.

Compile and run the Java program to import data.
---

## 🛠 Features
✅ Import transaction data from **Excel** to **MySQL** using Java  
✅ **Normalized database** structure with `Product`, `Category`, and `Transactions` tables  
✅ **REST API** built with **Node.js & Express.js** for data retrieval  
✅ **React Dashboard** with **filters** and **data visualization**  
✅ **Responsive UI** for easy navigation  

---

## 📂 Project Structure
project-root/ │── backend/ # Java (Excel to MySQL) │── server/ # Node.js Express API │── frontend/ # React.js Dashboard UI │── db/ # SQL scripts │── README.md # Documentation
---

## 📂 Database Schema

### **1. Category Table**
```sql
CREATE TABLE Category (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL UNIQUE
);


CREATE TABLE Product (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    category_id INT,
    FOREIGN KEY (category_id) REFERENCES Category(id)
);
CREATE TABLE Transactions (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_id INT,
    amount DECIMAL(10,2) NOT NULL,
    transaction_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (product_id) REFERENCES Product(id)
);
🚀 Setup Instructions
1️⃣ Backend (Java - Import Excel to MySQL)
Install MySQL and create a database.
Update database credentials in dbConfig.java.
Compile & run the Java program to import transactions.
2️⃣ Server (Node.js + Express API)
cd Backend
npm install
npx nodemon //run backend
3️⃣ Frontend (React.js Dashboard)
cd frontend
npm install
npm run dev//run frontend
🎯 API Endpoints
Method	Endpoint	Description
GET	/api/products	Fetch all products
GET	/api/categories	Fetch all categories
GET	/api/transactions	Fetch all transactions
🚀 Future Enhancements


🔐 Authentication & Authorization (JWT)
📊 Data Visualization (Charts for transactions)
📤 CSV Export & Import Feature

