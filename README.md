# Automotive Parts Database System

Fully normalized relational database for an automotive parts business. Designed in MySQL Workbench with a complete EER diagram, foreign key constraints, sample data insertion scripts, and optimized analytical queries.

## Stack

**Database** — MySQL / SQL Server  
**Design Tool** — MySQL Workbench 8.0  
**Language** — SQL  

## Schema

| Entity | Description |
|---|---|
| Parts | Catalog — part number, name, description, price, stock |
| Suppliers | Directory with contact info and lead times |
| Customers | B2B and retail customer records |
| Purchase Orders | Orders placed with suppliers to restock inventory |
| Sales Orders | Customer transactions with line items |
| Inventory | Current stock levels with movement history |

Normalized to 3NF. Foreign keys enforce referential integrity across all relationships.

## Key Design Decisions

- Separate `purchase_orders` and `sales_orders` tables for independent procurement vs. revenue reporting
- Indexes on commonly queried columns — part number, supplier ID, order date — for efficient lookups
- Stock levels derived from purchase receipts minus sales, with an adjustment table for manual corrections
- Cascading constraints prevent orphaned line items when order headers are modified

## Files

| File | Description |
|---|---|
| `automotive_database.mwb` | MySQL Workbench model — EER diagram + full schema |
| `schema.sql` | DDL — CREATE TABLE statements with all constraints |
| `data.sql` | Sample data for testing and demos |
| `queries.sql` | Analytical queries — stock check, order history, supplier performance |

## How to Open

1. Install [MySQL Workbench](https://www.mysql.com/products/workbench/) 8.0+
2. **File → Open Model → `automotive_database.mwb`** to view the EER diagram
3. Run `schema.sql` on your MySQL instance to create the database
4. Run `data.sql` to load sample data
5. Run queries from `queries.sql` to explore the schema

## Highlights

- Fully normalized to 3NF — zero data redundancy across all tables
- Complete EER diagram documenting all entities, attributes, and relationships
- Optimized queries covering stock checks, order history, and supplier performance

---

Built by Homer Palada — CS student at Universidad Católica de Honduras, graduating May 2027.
