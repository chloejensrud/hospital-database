# Hospital Database Management System

A relational database designed from the ground up to support hospital operations and patient information management, built by a multidisciplinary team from real-world healthcare business requirements.

My contribution: I was responsible for creating the database views, stored procedures, triggers, and functions. I also assisted with the creation of the Entity-Relationship Diagram (ERD).

Tools: MySQL, Lucid Chart, Excel, Word, 
Skills demonstrated: relational design, normalization, SQL (DDL/DML/joins/aggregation), healthcare workflow analysis, requirements gathering

---

## Overview

[2-3 sentences: What problem does this solve? Who would use it (registration staff, nurses, billing, administrators)? Example: "Hospitals need to track patients, their visits, the providers who treated them, and the services billed. This database models those workflows across X tables."]

**At a glance**
- **[X] tables** covering [patients, encounters, providers, departments, billing, etc.]
- **[Y] queries** answering real operational questions
- **Synthetic data only.** No real patient information is used.

---

## Entity Relationship Diagram

![ERD](docs/erd.png)

*[One sentence guiding the reader: "A patient can have many encounters; each encounter is handled by one provider and can have multiple diagnoses."]*

---

## Business Requirements

| # | Requirement | How the design supports it |
|---|-------------|----------------------------|
| 1 | [e.g., Track which physician treated which patient per admission] | [e.g., `Encounter` links `Patient` and `Provider`] |
| 2 | [e.g., Support multiple diagnoses per visit] | [e.g., Separate `Diagnosis` table linked to `Encounter`] |
| 3 | [add more] | |

---

## Design Decisions

- **Normalization:** [e.g., "Normalized to 3NF. Separated Diagnosis from Encounter to avoid repeating groups."]
- **Keys and constraints:** [e.g., primary keys, foreign keys, NOT NULL, CHECK constraints you used]
- **Tradeoffs:** [anything you'd do differently]

---

## Data Dictionary

Full version in [`docs/data_dictionary.md`](docs/data_dictionary.md).

| Table | Column | Type | Description |
|-------|--------|------|-------------|
| Patient | patient_id | INT (PK) | Unique patient identifier |
| [..] | [..] | [..] | [..] |

---

## Sample Queries

### 1. [Business question, e.g., "Which patients were readmitted within 30 days?"]
```sql
-- paste query here
```
![Query 1 result](screenshots/query1.png)

### 2. [Business question, e.g., "Bed occupancy by department"]
```sql
-- paste query here
```
![Query 2 result](screenshots/query2.png)

*[Add 5-8 total.]*

---

## Repository Structure

```
hospital-database/
├── README.md
├── docs/
│   ├── erd.png
│   └── data_dictionary.md
├── sql/
│   ├── schema.sql
│   ├── sample_data.sql
│   └── queries.sql
└── screenshots/
```

## How to Run

1. Create a database: `CREATE DATABASE hospital;`
2. Run `sql/schema.sql` to create the tables.
3. Run `sql/sample_data.sql` to load synthetic data.
4. Run the queries in `sql/queries.sql`.

---

## What I Learned

[2-3 sentences: a challenge you hit and how you solved it, or what you'd improve with more time.]

## Data Privacy Note

All data in this repository is synthetic and created for educational purposes.
