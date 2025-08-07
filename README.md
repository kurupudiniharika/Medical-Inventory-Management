# Medical-Inventory-Management

## 🏥 **Medical Inventory Management System**

**Platform:** Salesforce Developer Edition
**Type:** Internship/Academic Project
**Technology:** Salesforce CRM (Admin + Declarative + Automation)

---

### 🔧 **Hardware/Software Requirements**

* **Device**: Laptop/Desktop
* **Internet**: Required
* **Salesforce Developer Org**: Free edition
* **VS Code** (optional for SFDX operations)
* **Browser**: For interaction with Lightning App UI

---

### 📘 **Project Objective / User Story**

> A complete Medical Inventory Management System built on Salesforce to manage and streamline various aspects of hospital or clinic inventory. It ensures efficient tracking of suppliers, purchase orders, product inventory, transactions, expiry date alerts, and more. The goal is to improve operational efficiency, data accuracy, and real-time monitoring using Salesforce’s declarative tools.

---

### 🔨 **Key Components Built**

#### 1. **Custom Objects**

| Object             | Fields                                                                               |
| ------------------ | ------------------------------------------------------------------------------------ |
| **Product**        | Product Name, Batch Number, Quantity, Expiry Date, Manufacture Date, Supplier Lookup |
| **Supplier**       | Name, Contact Info, Address, Email                                                   |
| **Purchase Order** | Supplier Lookup, Order Date, Products (via junction object)                          |
| **Transaction**    | Product Lookup, Transaction Type (Issue/Receive), Quantity, Date                     |

#### 2. **Relationships**

* Lookup and Master-Detail Relationships:

  * Supplier ↔ Product (Lookup)
  * Purchase Order ↔ Products (via junction object)
  * Product ↔ Transactions (Lookup)

#### 3. **Validation Rules**

* Ensure:

  * `Expiry_Date > Manufacture_Date`
  * Quantity cannot be negative
  * Mandatory fields not left blank

#### 4. **Automation using Flows**

| Flow Type            | Use Case                                              |
| -------------------- | ----------------------------------------------------- |
| **Record-Triggered** | Update stock when new transaction is logged           |
| **Scheduled Flow**   | Daily check for near-expiry and expired products      |
| **Screen Flow**      | Guided form to create Purchase Orders or Transactions |

#### 5. **Apex Triggers (Optional if needed)**

* Auto-adjust stock quantities
* Restrict deletion of related records

#### 6. **Reports**

* Expired Products
* Low Stock Items
* Supplier-based Orders
* Product Transaction History

#### 7. **Dashboards**

* Pie Charts for:

  * Product Expiry Status (Valid / Expired / Near Expiry)
* KPI Metrics:

  * Total Products in Stock
  * Total Expired
  * Total Orders Issued
* Bar Charts: Purchase Orders per Supplier

#### 8. **Roles and Profiles**

| Role                         | Access                             |
| ---------------------------- | ---------------------------------- |
| Admin                        | Full access                        |
| Inventory Manager            | Create/Update Products, Orders     |
| Viewer                       | Read-only reports                  |
| Supplier Role                | Limited visibility of own supplies |

#### 9. **Lightning App Builder**

* Built a **custom app**: `MedicalInventoryManagement`
* Custom Tabs:

  * Products
  * Suppliers
  * Orders
  * Transactions
* Custom Navigation Menu and Branding
* Option to expose tabs/pages using Experience Cloud (site deployment)

---




