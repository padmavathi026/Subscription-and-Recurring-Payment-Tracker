# Subscription-and-Recurring-Payment-Tracker
<h1>💳 Subscription and Recurring Payment Tracker</h1>

<h2>Description</h2>
A relational database project to efficiently manage and analyze recurring payments and subscription services like Netflix, Spotify, Amazon Prime, and more. This system aims to replace error-prone spreadsheet methods with a normalized, scalable, and constraint-validated PostgreSQL database along with an interactive web interface for query execution.

<h3> Problem Statement</h3>
With the growth of the subscription economy, users face difficulty tracking billing cycles, renewal dates, payment statuses, and spending habits. This project builds a robust database-backed system to:

- Track and manage subscription details.

- Send automated reminders for upcoming bills.

- Provide analytical insights on spending and service usage.

<h4>🧱 Key Features</h4>

- 🔄 Transformed dataset into different tables.
  
- 🔄 Took 50% of the dataset for testing and debugging in a separate database.
  
- 🔄 Created MainDB that has 100% of the transformed dataset.
  
- 🔄 Normalized PostgreSQL Schema (BCNF/3NF)

- 🔐 Strong Data Integrity via constraints and referential keys (chase test done).

- 📉 Spending Analytics via JOIN, GROUP BY, and subqueries

- 📨 Reminder Notifications system per user/subscription

- 📊 Web Interface (Streamlit) for custom SQL execution


<h5>📂 Project Structure </h5>

-Milestone2/
-├── create_tables.sql            # DDL for table creation
-├── insert_sample_data.sql       # Sample test data
-├── optimized_queries.sql        # Final tuned SQL queries
-├── streamlit_app/
-│   └── app.py                   # SQL Runner Web Interface (Streamlit)
-└── Milestone2.pdf               # Full project report and documentation


<h6> 🧮 Database Design </h6>
<b>👥 Main Entities:</b>

- Users – email, phone, is_active

- Services – like Netflix, Amazon Prime

- Subscriptions – details like billing cycle, auto-renew, amount

- Payments – records of all user payments

- Notification_Messages – alerts about upcoming bills

- Billing_Cycles, Categories, Payment_Methods, Subscription_Status

<b> ✅ Constraints: </b>
- CHECK (amount >= 0) for payment logic

- Valid email/phone formats

- Full primary/foreign key integrity across tables

- Indexes for performance on large datasets
  
<h7>🔄 Normalization:</h7>

- Fully normalized to BCNF using functional dependency analysis and decomposition

- Decomposed Payments and Notifications into new logical tables
  
<h8> 🚀 Web Interface (Streamlit) </h8>

An interactive website (http://localhost:8501) was developed using Streamlit for real-time SQL operations.

<b> 🛠️ Tech Stack </b>
Frontend: Streamlit

Backend: PostgreSQL

Connector: psycopg2

Query Display: Pandas tables

<b> 🔍 Supported Operations </b>
- Run SELECT, INSERT, UPDATE, DELETE SQL queries

- Display live query output or success messages

<h9>  📈 Performance Tuning </h9>
- Indexes added on high-frequency join/filter columns

- Optimized plans used Index Scan, Hash Join instead of Seq Scan

- Query plans analyzed using EXPLAIN

<h10> 🔒 Data Validation Highlights </h10>
- No duplicate primary keys

- No nulls in required fields

- Logical validation on email, phone, subscription amounts

- Referential checks passed across all foreign keys




