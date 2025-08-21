# 📦 Medical Inventory Management (Salesforce Project)

## 📖 Overview
The **Medical Inventory Management System** is a Salesforce-based solution designed to efficiently track and manage medical products, suppliers, purchase orders, and stock transactions.  
The project uses **Custom Objects, Relationships, Validation Rules, Flows, Apex Triggers, Reports, and Dashboards** to automate and streamline the healthcare inventory process.

**Platform:** Salesforce Developer Edition
**Technology:** Salesforce CRM (Admin + Declarative + Automation)
---

## 🏆 Project Milestones  

### 📌 1. Object Creation  

**Custom Objects & Key Fields**
- **Product** → Product ID, Unit Price, Product Name, Current Stock Level, Product Description, Minimum Stock Level 
- **Supplier** → Name, ID, Contact Person, Location, Email, Phone Number, Address 
- **Purchase Order** → Order ID, Supplier ID Lookup, Order Date, Status, Expected Delivery Date, Actual Delivery Date, Total Order Cost
- **Inventory Transaction** → Product Lookup, Transaction Type (Issue / Receive), Quantity, Date
- **Order Items** → Order Item ID, Purchase Order ID, Quantity Ordered, Quantity Received, Product Lookup

**Relationships**
- Supplier ↔ Product → Lookup  
- Purchase Order ↔ Products → Junction Object  
- Product ↔ Transactions → Lookup  

---

### 📌 2. Validation Rules  
Ensure:
- **Expiry_Date > Manufacture_Date**  
- **Quantity ≥ 0** (no negative values)  
- Mandatory fields must not be left blank  

---

### 📌 3. Automation with Flows  

| Flow Type          | Purpose |
|--------------------|---------|
| **Record-Triggered** | Update stock automatically when a new transaction is logged |
| **Scheduled Flow**   | Daily check for near-expiry and expired products |
| **Screen Flow**      | Guided form to create Purchase Orders or Transactions |

---

### 📌 4. Apex Triggers 
- Automatically adjust stock quantities after transactions  
- Restrict deletion of related records (e.g., prevent deleting a product with active transactions)  

---

### 📌 5. Profiles & Roles  
- **Admin** → Full access to all objects and automation  
- **Inventory Manager** → Can create and update Products, Transactions, and Purchase Orders  
- **Supplier Role** → Limited access to related records only  

---

### 📌 6. Reports  
- **Expired Products** → List of expired items  
- **Low Stock Items** → Products below threshold quantity  
- **Supplier-based Orders** → Orders grouped by supplier  
- **Product Transaction History** → Full transaction log per product  

---

#### 📌 7. **Dashboards**

* Pie Charts for:

  * Product Expiry Status (Valid / Expired / Near Expiry)
* KPI Metrics:

  * Total Products in Stock
  * Total Expired
  * Total Orders Issued
* Bar Charts: Purchase Orders per Supplier


#### 📌 8. **Lightning App Builder**

* Built a **custom app**: `MedicalInventoryManagement`
* Custom Tabs:

  * Products
  * Suppliers
  * Orders
  * Transactions
* Custom Navigation Menu and Branding
* Option to expose tabs/pages using Experience Cloud (site deployment)

---




