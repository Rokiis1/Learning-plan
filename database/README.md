# Table of Contents

- [Relational Databases](#relational-databases)
    - [Overview](#overview-relational)
    - [Characteristics](#characteristics-relational)
    - [Use Cases](#use-cases-relational)
- [NoSQL Databases](#nosql-databases)
    - [Document Databases](#document-databases)
        - [Overview](#overview-document)
        - [Characteristics](#characteristics-document)
        - [Use Cases](#use-cases-document)
    - [Key-Value Databases](#key-value-database)
        - [Overview](#overview-key-value)
        - [Characteristics](#characteristics-key-value)
        - [Use Cases](#use-cases-key-value)

# Relational Databases

## Relational Databases

Relational databases are based on the relational model of data, where data is organized into tables with rows and columns. They use structured query language (SQL) for defining, manipulating, and retrieving data. Relational databases establish relationships between tables using primary and foreign keys, enabling efficient data retrieval and data integrity enforcement.

## Characteristics

- Structured data model based on tables, rows, and columns.
- Strong data consistency and ACID (Atomicity, Consistency, Isolation, Durability) properties.
- Support for complex queries and joins.
- Ability to enforce data integrity using constraints.
- Well-established and widely adopted technology.
- Suitable for structured and tabular data.

## Use Cases

- Business applications with well-defined and structured data requirements.
- Financial systems for storing transactional data.
- Data-driven applications requiring complex queries and aggregations.
- Applications requiring strong data consistency and integrity.

# NoSQL Databases

## Document Databases

### Overview

Document databases are part of the NoSQL family and store data in flexible, semi-structured documents (e.g., JSON, XML). They provide high flexibility by allowing different documents within the same collection to have different structures. Document databases offer a schemaless design, making it easier to handle evolving data schemas and adapt to changing requirements.

### Characteristics

- Flexible data model using documents (e.g., JSON, XML) with key-value pairs.
- No fixed schema, allowing documents within a collection to have different structures.
- Queries are typically performed using document-based query languages or indexing mechanisms.
- Horizontal scalability and distributed database systems.
- Good performance for read-heavy workloads.

### Use Cases

- Content management systems with dynamic and evolving data structures.
- Applications dealing with semi-structured or unstructured data.
- Personalization and recommendation systems.
- Collaborative environments and social networks.

## Key-Value Databases

### Overview

Key-value databases are another type of NoSQL database that stores data as a collection of key-value pairs. They provide a simple and efficient way to store and retrieve data using a unique identifier (key). Key-value databases excel at handling high-volume read and write operations and are often used as caching layers or for storing metadata.

### Characteristics

- Data model based on simple key-value pairs.
- High scalability and performance for read and write operations.
- Minimal query functionality (usually limited to key-based retrieval).
- Highly flexible and schemaless design.
- Distributed systems with eventual consistency guarantees.

### Use Cases

- Session management and user profiles in web applications.
- Caching layers for improving performance.
- Storing metadata, configurations, and settings.
- Message queues and distributed systems.