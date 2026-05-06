# Automotive Parts Database System

Relational database design for an automotive parts business — modeled in MySQL Workbench with normalized schema, foreign key constraints, and query optimization for inventory and sales operations.

## Tech Stack

- **Database** — MySQL / SQL Server
- **Design Tool** — MySQL Workbench (`.mwb`)
- **Query Language** — SQL

## Schema Overview

The database covers the core entities of an automotive parts store:

- **Parts** — catalog of automotive parts with part number, name, description, price, and stock
- **Suppliers** — supplier directory with contact info and lead times
- **Customers** — customer records for B2B and retail accounts
- **Purchase Orders** — orders placed with suppliers to restock inventory
- **Sales Orders** — sales transactions to customers with line items
- **Inventory** — current stock levels with movement history

## Key Design Decisions

- Fully normalized to 3NF to eliminate data redundancy
- Foreign key constraints enforce referential integrity across all relationships
- Indexed on commonly queried columns (part number, supplier ID, order date) for efficient lookups
- Separated purchase and sales order tables to support independent reporting

## Files

| File | Description |
|---|---|
| `automotive_database.mwb` | MySQL Workbench model — open with MySQL Workbench 8.0+ |

## How to Open

1. Install [MySQL Workbench](https://www.mysql.com/products/workbench/)
2. File → Open Model → select `automotive_database.mwb`
3. View the EER diagram and schema under the **Model** tab

## Highlights

- Designed a fully normalized relational database from scratch for a real business domain
- Applied foreign key constraints and indexes to ensure data integrity and query performance
- Schema supports inventory tracking, supplier management, and customer sales workflows
- Optimized common queries (parts lookup, stock check, order history) through indexed columns
