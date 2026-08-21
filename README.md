# Regulatory Data SQL Portfolio Project

## Project Overview

This is a personal SQL portfolio project based on a simplified regulatory data environment.

The project demonstrates the design and analysis of a relational database containing regulatory documents, publishers, jurisdictions and regulatory topics.

It was created to develop and demonstrate practical SQL skills using a realistic regulatory-data scenario.

## Project Objectives

* Design a relational database structure for regulatory information.
* Create tables using primary and foreign key relationships.
* Populate the database with regulatory publishers, jurisdictions, documents and topics.
* Model many-to-many relationships between regulatory documents and topics.
* Use SQL to retrieve, filter, validate and analyse structured data.
* Perform analysis across multiple related tables.
* Apply aggregation, grouping, conditional logic and Common Table Expressions (CTEs).

## Database Structure

The database contains five related tables:

### `publishers`

Stores information about regulatory authorities and other regulatory publishers.

Key fields:

* `publisher_id`
* `publisher_name`
* `country`
* `website`

### `jurisdictions`

Stores the jurisdictions associated with regulatory documents.

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

Stores regulatory subject areas used to classify regulatory documents.

Key fields:

* `topic_id`
* `topic_name`

### `document_topics`

A junction table connecting regulatory documents with regulatory topics.

This allows one regulatory document to be linked to multiple topics and one topic to be associated with multiple documents, demonstrating a many-to-many relational database relationship.

Key fields:

* `document_id`
* `topic_id`

## Dataset

The project currently contains:

* **10 jurisdictions**
* **20 regulatory publishers**
* **30 regulatory documents**
* **10 regulatory topics**
* **37 document-topic relationships**

The dataset combines fictional project records with selected publicly available regulatory document references and publisher websites for portfolio and learning purposes.

No employer or confidential data is used in this project.

## SQL Analysis

The analysis queries demonstrate the use of:

* `SELECT`
* `WHERE`
* `AND`
* `IN`
* `ORDER BY`
* `INNER JOIN`
* `LEFT JOIN`
* Multi-table `JOIN`
* `COUNT()`
* `GROUP BY`
* `HAVING`
* `CASE`
* Common Table Expressions (`CTEs`)
* Date-based filtering
* Aggregate-result filtering

Example analytical questions include:

* Which regulatory documents are currently active?
* Which document types are represented in the dataset?
* How many documents does each publisher have?
* How many documents are associated with each jurisdiction?
* Which jurisdictions contain multiple recent regulatory documents?
* How can regulatory documents be categorised based on their status?
* How are regulatory documents connected to regulatory topics?
* How many active documents are associated with each topic?
* Which publishers have multiple active regulatory documents?
* Which document types contain multiple active documents?
* How can CTEs be used to prepare aggregated results before further filtering and analysis?

## Example CTE Analysis

The project includes Common Table Expressions used to:

* Count documents by publisher.
* Analyse recent documents by jurisdiction.
* Count active documents by regulatory topic.
* Analyse active documents by document type.
* Filter aggregated results based on document counts.
* Join CTE results with reference tables to display readable publisher, jurisdiction and topic names.

These queries combine CTEs with filtering, aggregation, `GROUP BY`, joins and ordering.

## Repository Structure

```text
regulatory-data-sql-portfolio/
│
├── README.md
│
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_insert_data.sql
│   └── 03_analysis_queries.sql
│
└── screenshots/
