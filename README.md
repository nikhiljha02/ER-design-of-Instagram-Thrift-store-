# E-Commerce ER Diagram

## Overview
This project models a simple e-commerce system with key entities: Customers, Products, Orders, OrderItems, Payments, and Shipping.

## Entities & Relationships

- **Customers**  
  One customer can place many orders.  
  *(1 Customer → Many Orders)*

- **Orders**  
  Each order belongs to one customer and contains multiple order items.  
  *(1 Order → Many OrderItems)*

- **OrderItems**  
  Each order item references exactly one product.  
  *(Many OrderItems → 1 Product)*

- **Products**  
  Products have attributes like `productTag` (e.g., thrift, handmade), price, condition, and supplier.

- **Payments**  
  Each order has exactly one payment record.  
  *(1 Order → 1 Payment)*

- **Shipping**  
  Each order has exactly one shipping detail.  
  *(1 Order → 1 Shipping)*

## Design Notes

- Product types are distinguished via an enum in the products table for simplicity.
- Payment and shipping link to orders, not directly to customers.
- This design ensures clear, normalized tracking of orders, products, payments, and shipments.

---

Feel free to contribute or raise issues for improvements!
