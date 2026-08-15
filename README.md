# Regulatory Data SQL Project

## Project Overview

This project is a personal SQL portfolio project based on a simplified regulatory data environment.

The purpose of the project is to design a relational database for regulatory documents and use SQL to analyse relationships between regulatory documents, publishers, jurisdictions and regulatory topics.

The project was created to develop practical SQL skills using a realistic regulatory-data scenario.

## Project Objectives

* Design a relational database structure for regulatory information.
* Create tables with primary and foreign key relationships.
* Populate the database with regulatory publishers, jurisdictions, documents and topics.
* Model many-to-many relationships between documents and regulatory topics.
* Use SQL queries to explore and analyse the dataset.
* Practise data filtering, sorting, aggregation and relational joins.

## Database Structure

The database contains five tables:

### `publishers`

Stores information about regulatory authorities and other regulatory publishers.

Key fields:

* `publisher_id`
* `publisher_name`
* `country`
* `website`

### `jurisdictions`

Stores the jurisdictions covered by the regulatory documents.

Key fields:

* `jurisdiction_id`
* `jurisdiction_name`
* `region`

### `regulatory_documents`

Stores regulatory document metadata.

Key fields:

* `document_id`
* `title`
* `publisher_id`
* `jurisdiction_id`
* `document_type`
* `publication_date`
* `effective_date`
* `status`
* `source_url`
* `description`

### `topics`

Stores regulatory subject areas.

Examples include:

* Anti-Money Laundering
* Consumer Protection
* Prudential Regulation
* MiFID II
* Risk Management
* Capital Requirements
* ICT and Operational Resilience

### `document_topics`

A junction table connecting regulatory documents with regulatory topics.

This allows a document to be associated with multiple topics and demonstrates a many-to-many relational database design.

## Dataset

The project currently contains:

* **10 jurisdictions**
* **20 regulatory publishers**
* **30 regulatory documents**
* **10 regulatory topics**
* **37 document-topic relationships**

The dataset combines fictional project records with selected real-world regulatory document references and publisher websites for portfolio and learning purposes.

## SQL Analysis

The analysis queries demonstrate:

* `SELECT`
* `WHERE`
* `IN`
* `ORDER BY`
* `LEFT JOIN`
* `JOIN`
* `COUNT()`
* `GROUP BY`
* `HAVING`
* `CASE`

Example analytical questions include:

* Which regulatory documents are currently active?
* Which document types are represented in the dataset?
* How many documents does each publisher have?
* How many documents are associated with each jurisdiction?
* Which jurisdictions have more than two documents?
* How can documents be categorised based on their status?
* How are regulatory documents connected to regulatory topics?

## Repository Structure

```text
regulatory-data-sql-project/
│
├── README.md
│
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_insert_data.sql
│   └── 03_analysis_queries.sql
│
└── screenshots/
```

### SQL files

**`01_create_tables.sql`**
Contains the database table definitions, primary keys and foreign key relationships.

**`02_insert_data.sql`**
Contains the data insertion statements used to populate the database.

**`03_analysis_queries.sql`**
Contains SQL analysis queries developed during the project.

## Tools

* PostgreSQL
* Supabase SQL Editor
* SQL
* GitHub

## Skills Demonstrated

This project demonstrates developing/intermediate SQL skills, including relational database design, joins, aggregation, filtering, grouping and conditional logic.

The project is being developed alongside continued SQL learning, with plans to extend the analysis using additional SQL techniques.

## Project Development

This is an ongoing learning project. Future improvements may include:

* More complex multi-table analysis
* Subqueries
* Common Table Expressions (CTEs)
* Additional date-based analysis
* More advanced aggregation
* Data quality checks
* Further regulatory data analysis
