# Transaction Fraud Detection Dashboard (Credit Card Transactions)

This project analyzes credit card transaction data specifically aimed at fraud detection using rule-based systems. It utilizes PostgreSQL for data storage and Grafana for insightful, interactive visualizations.

---
<img src="/Users/vaidehipawar/Desktop/grafana/assets/Dashboard.png" alt="Dashboard Screenshot" width="600px"/>

## 🚀 Overview

The dashboard provides insights into:

* **Fraud detection rule triggers**
* **Transaction type distribution**
* **Approved and rejected transactions**
* **Blacklisted account activities**

---

## 🛠 Technologies Used

* **Database**: PostgreSQL
* **Visualization Tool**: Grafana
* **Data Generation**: Python (Faker library)

---

## 📌 Field Descriptions

* **Uniq\_id** – Unique ID for each transaction
* **Trans\_type** – Type of transaction categorized into:

  * **Real\_time\_transaction**: Real-time transactions (e.g., grocery store purchases using credit cards)
  * **Settlements**: Transactions involving funds transfer through clearinghouses (payer's bank debits, payee's bank credits)
  * **Dispute**: Reversed transactions when customers dispute charges
* **Amount** – Transaction amount
* **Amount\_crr** – Transaction amount converted into different currencies (e.g., INR, USD)
* **Account\_holder\_name** – Name of the account holder
* **Card\_presence** – Indicates if the card was present during the transaction (Present/Not present)
* **Merchant\_category** – Merchant transaction categories (e.g., gambling, flight tickets, grocery stores)
* **Card\_type** – Type of card (e.g., Mastercard, Visa)
* **Card\_id** – Unique identifier for credit cards (banks generate new IDs periodically)
* **Account\_id** – Unique identifier for customer accounts
* **Account\_blacklisted** – Indicates if an account is blacklisted
* **Rules\_triggered** – Fraud rules triggered by the transaction
* **Rules\_explanation** – Explanation detailing why the rule was triggered
* **Decision** – Outcome of transaction evaluation (Approved/Rejected)

---

## 📈 Grafana Dashboards

### Panels Included:

* **Rejected Transaction Count (Stat)**
* **Approved Transaction Count (Stat)**
* **Total Approved Transaction Amount (Stat)**
* **Total Rejected Transaction Amount (Stat)**
* **Transaction Types Distribution (Pie Chart)**
* **Rules Triggered Analysis (Bar Chart)**
* **Blacklisted Account Activity (Bar Chart)**

---

## 🖥 Setup Instructions

### 1. Clone Repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Python Environment Setup

```bash
conda create -n fraud_detection python=3.8 -y
conda activate fraud_detection
pip install -r requirements.txt
```

### 3. PostgreSQL Database Setup

* Setup PostgreSQL database instance (local or cloud).
* Run the provided Python scripts to create and populate the `banking_data` table.

### 4. Grafana Setup

* Install Grafana from [Grafana Official Site](https://grafana.com/docs/grafana/latest/setup-grafana/installation/).
* Configure PostgreSQL as a Grafana data source.
* Import or manually create dashboard panels using provided queries.

---

## 📦 Dependencies

* Python 3.8
* psycopg2
* pandas
* Faker
* Grafana
* PostgreSQL

---

## 🎯 Usage

Run the Python script for continuous data generation, and monitor real-time insights via Grafana. Customize dashboards based on required analytical needs.

---

## 📧 Contact

For questions or support, reach out to the project maintainer at:

* pawar.vaidehi612@gmail.com

---

