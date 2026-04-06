# 🛒 E-Commerce ER Diagram (Instagram Thrift Store)

## 📌 Overview

This project represents an **Entity-Relationship (ER) Diagram** for an Instagram-based thrift store.
It models how core components of an e-commerce system interact, including **customers, products, orders, payments, and shipping**.

The goal of this design is to provide a **clear database structure** for managing product listings, customer orders, and transaction workflows.

---

## 🧱 Entities in the System

### 👤 Customers

Stores information about users who place orders.

**Attributes:**

* customer_id (PK)
* name
* email
* address

**Relationship:**

* One customer can place multiple orders *(1:N)*

---

### 📦 Products

Represents items available for sale in the thrift store.

**Attributes:**

* product_id (PK)
* product_name
* description
* price
* stock
* category
* condition

**Relationship:**

* A product can appear in multiple order items

---

### 🧾 Orders

Represents a purchase made by a customer.

**Attributes:**

* order_id (PK)
* customer_id (FK)
* order_date
* status
* total_amount

**Relationship:**

* Each order belongs to one customer *(N:1)*
* One order contains multiple order items *(1:N)*

---

### 🧩 OrderItems

Acts as a **junction table** between Orders and Products.

**Attributes:**

* order_item_id (PK)
* order_id (FK)
* product_id (FK)
* quantity
* price

**Purpose:**

* Resolves the **many-to-many relationship** between orders and products

---

### 💳 Payments

Stores payment details for each order.

**Attributes:**

* payment_id (PK)
* order_id (FK)
* payment_method
* payment_status
* amount

**Relationship:**

* One order has one payment *(1:1)*

---

### 🚚 Shipping

Stores delivery details for orders.

**Attributes:**

* shipping_id (PK)
* order_id (FK)
* address
* city
* delivery_status
* tracking_number

**Relationship:**

* One order has one shipping record *(1:1)*

---

## 🔗 Relationships Summary

* **Customer → Orders** = One-to-Many
* **Orders → OrderItems** = One-to-Many
* **Products → OrderItems** = One-to-Many
* **Orders → Payments** = One-to-One
* **Orders → Shipping** = One-to-One

This structure ensures proper normalization and avoids data redundancy while maintaining scalability.

---

## 🧠 Key Concepts Used

* **Primary Keys (PK):** Unique identifiers for each entity
* **Foreign Keys (FK):** Used to connect related entities
* **Normalization:** Eliminates redundancy
* **Associative Entity:** OrderItems resolves many-to-many relationships

---

---

## 🚀 Use Cases

* Build a backend database for an e-commerce app
* Practice database design concepts
* Learn ER modeling for real-world systems
* Portfolio project for interviews

---

## 🛠️ Future Improvements

* Add **User Authentication system**
* Include **Product Reviews & Ratings**
* Add **Cart/Wishlist functionality**
* Normalize product categories into a separate table
* Add **Admin panel support**

---

## 👨‍💻 Author

**Nikhil Kumar Jha**

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!
