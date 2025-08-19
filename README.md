![Mysql](https://img.shields.io/badge/Tool-Mysql-darkgreen) ![PLSQL](https://img.shields.io/badge/Tool-PL%2FSQL-purple)  
![Feedback](https://img.shields.io/badge/Output-Customer_Feedback-orange)  
![Completed](https://img.shields.io/badge/Status-Completed-success)  



#  Online Food Delivery Order & Feedback System

This project is a SQL-based backend system built to manage online food delivery workflows, from order placement to customer feedback. It is designed using SQL Developer and includes triggers, procedures, views, and relational constraints.

---

## 📌 Project Objective

To simulate and manage the backend operations of an online food delivery platform that handles:
- Customer orders
- Delivery status and performance
- Feedback and ratings

---

## 🧰 Tools & Technologies

- **SQL Developer**
- **MySQL / Oracle SQL**
- **PL/SQL Constructs (Triggers, Procedures)**
- **Views and Relational Constraints**

---

## 🛠️ Key Features

- 📦 **Order Management**  
  Create, update, and track food orders with delivery assignments.

- 🚴 **Delivery Monitoring**  
  Keep records of delivery staff, delivery times, and performance.

- ⭐ **Feedback System**  
  Customers can rate and provide feedback on their experience.

- 🔐 **Data Integrity**  
  Enforced using:
  - Foreign key constraints
  - Triggers for validation
  - Views for simplified reporting

---

## 🗂️ Database Structure

Typical entities in this system may include:
- `Customers`  
- `Orders`  
- `DeliveryStaff`  
- `Feedback`  
- `Restaurants`  
- `MenuItems`


## 🔄 SQL Components Used

| Component   | Description                                 |
|------------|---------------------------------------------|
| Tables      | Stores normalized data for each entity      |
| Triggers    | Automate actions like logging and validation|
| Procedures  | Encapsulate order creation and assignment   |
| Views       | Aggregate data for admin reports            |
| Constraints | Enforce referential integrity               |

---

## 🧪 Sample SQL Snippets

sql
CREATE OR REPLACE TRIGGER prevent_invalid_rating
BEFORE INSERT ON Feedback
FOR EACH ROW
BEGIN
  IF :NEW.rating < 1 OR :NEW.rating > 5 THEN
    RAISE_APPLICATION_ERROR(-20001, 'Rating must be between 1 and 5.');
  END IF;
END;


## ✅ How to Use

1. Open the project in **SQL Developer**.
2. Run the provided SQL scripts to create the schema.
3. Insert test data or use `INSERT` statements to simulate orders.
4. Use procedures to handle new orders and delivery.
5. View reports using predefined `VIEW` statements.

---

## 👨‍💻 Author

**Shubham Ghalsasi**
Final Year B.Tech – Cloud Computing
MIT ADT University
📫 [ghalsasishubham@gmail.com](mailto:ghalsasishubham@gmail.com)

