🏫 School Kids Organizer (SQL + Python Automation Engine)

📌 Project Overview

School Kids Organizer is a Python-driven automation system designed to eliminate manual administrative overhead in allocating children to preschool groups. 
By coupling Object-Oriented Programming (OOP) with a robust PostgreSQL database acting as the Single Source of Truth (SSOT), the system dynamically processes enrollment queues, validates capacity constraints, and balances group demographics (age, gender ratio, and capacity load).

Status: 🚧 Active Development (Passion Project / Side-Hustle)

💡 Key Features & Domain Logic

- Domain-Driven Design (OOP): Encapsulates core business entities into Python classes (`Child`, `Group`, `Kindergarten`) to maintain clean code and business logic separation.
- Single Source of Truth: All transactional states, capacity limits, and child profiles persist strictly in PostgreSQL.
- Smart Group Balancing Algorithm: Automatically assigns children based on:
  - Age Appropriateness: Matching children to targeted development age brackets.
  - Gender Balance: Maintaining equal gender ratios across newly formed groups.
  - Capacity & Load Optimization: Distributing intake evenly across available room limits.
- Command Line Interface (CLI): Lightweight CLI execution for system administrators to trigger allocations and inspect real-time group limits.

🛠️ Tech Stack & Methodology

- Language: Python 3.x (Object-Oriented Programming, CLI)
- Database Engine: PostgreSQL
- Database Connector: `psycopg2` / `SQLAlchemy`
- Concepts Applied: Object-Oriented Programming (OOP), Data Validation, Relational Database Modeling, CRUD Operations, Algorithmic Data Allocation.

🏗️ System Architecture & Class Model

```text
               +-----------------------+
               |     Kindergarten      | (Manages total facilities & logic)
               +-----------+-----------+
                           | 1
                           |
                           | *
                 +---------+---------+
                 |       Group       | (Enforces max capacity & ratios)
                 +---------+---------+
                           | 1
                           |
                           | *
                 +---------+---------+
                 |       Child       | (Stores age, gender, assignment status)
                 +-------------------+
```
Child: Represents individual enrollment data (ID, age, gender, group ID).

Group: Tracks capacity limits, current occupancy, gender distribution, and age thresholds.

Kindergarten: High-level controller orchestrating database fetches, constraint checks, and allocation execution.

👨‍💻 Author
Daniel Żebrowski

Aspiring Data Analyst | SQL, Power BI & Python

LinkedIn: [Daniel Żebrowski](https://www.linkedin.com/in/daniel-%C5%BCebrowski-7a0937211/)

GitHub: @DanielZebrowski-Data
