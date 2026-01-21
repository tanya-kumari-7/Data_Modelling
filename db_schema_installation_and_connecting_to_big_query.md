# DbSchema Installation & Connecting to BigQuery

This guide explains **how to install DbSchema** and **connect it to Google BigQuery (BQ)** for data modeling and schema design.

---

## 1. What is DbSchema?

**DbSchema** is a **visual database modeling tool** used to:
- Design schemas using ER diagrams
- Define tables, PKs, FKs, and relationships
- Reverse engineer existing databases
- Generate SQL scripts

It supports **offline modeling** and **cloud databases**, including BigQuery.

---

## 2. Prerequisites

Before starting, ensure you have:

- Google Cloud Project
- BigQuery enabled in the project
- BigQuery permissions:
  - `BigQuery User` or `BigQuery Admin`
- Java (JDK 11+ recommended)
- Internet connection

---

## 3. Installing DbSchema (Mac)

### 3.1 Download DbSchema

1. Go to the official DbSchema website
2. Download **DbSchema for macOS (.dmg)**

### 3.2 Install

1. Open the `.dmg` file
2. Drag **DbSchema** to Applications
3. Launch DbSchema

✅ DbSchema is now installed

---

## 4. BigQuery Connection Overview

DbSchema connects to BigQuery using:
- **JDBC driver**
- **Service Account authentication**

BigQuery is treated as a **cloud database**.

---

## 5. Create BigQuery Service Account

1. Open **Google Cloud Console**
2. Go to **IAM & Admin → Service Accounts**
3. Click **Create Service Account**
4. Assign roles:
   - BigQuery User
   - BigQuery Data Viewer (or Admin if required)
5. Create and download **JSON key file**

⚠️ Store the key securely

---

## 6. Download BigQuery JDBC Driver

1. Download **Simba BigQuery JDBC Driver**
2. Extract the driver folder
3. Note the path to the `.jar` file

Example:
```text
/Users/username/Drivers/BigQueryJDBC42.jar
```

---

## 7. Connecting DbSchema to BigQuery

### 7.1 Create New DbSchema Project

1. Open DbSchema
2. Click **New Project**
3. Choose **Connect to Database**

---

### 7.2 Configure BigQuery Connection

Fill the following details:

- **Database Type:** BigQuery
- **Project ID:** `my_gcp_project`
- **Default Dataset:** `sales_schema`
- **Authentication:** Service Account JSON
- **Key File Path:** `/path/to/key.json`
- **JDBC Driver:** Select BigQuery JDBC `.jar`

Click **Test Connection**

✅ Connection successful

------------------

---
