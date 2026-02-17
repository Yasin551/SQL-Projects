# 🛒 Retail Sales Database Design

## 📌 Overview
This project presents a relational database schema designed for a retail sales management system.  
It models product management, customer data, orders, stores, territories, and staff operations.

## 🗂 Database Structure
The schema includes the following main entities:

- Customers
- Orders
- Products
- Categories & Subcategories
- Stores
- Staffs
- Territories

The `orders` table acts as the central fact table connecting customers, products, stores, staff, and territories.

## 🔗 Key Relationships
- Products → Categories → Subcategories  
- Orders → Customers  
- Orders → Products  
- Orders → Stores  
- Orders → Staffs  
- Orders → Territories  

## 🎯 Purpose
This project demonstrates:
- Relational database design
- Primary & Foreign key relationships
- Data normalization concepts
- Real-world retail data modeling

## 🛠 Tools Used
- drawSQL (Schema Design)
- SQL Concepts

---

<img width="4742" height="2116" alt="drawSQL-image-export-2026-02-17 (1)" src="https://github.com/user-attachments/assets/6d35ce8d-f468-4399-bc45-e08b4ce1ea00" />

