# Domain Context — Simple Stock Flow

## 1. Business Environment
**Simple Stock Flow** operates within the retail and inventory management domain. In this environment, maintaining absolute synchronization between physical stock and digital records is critical to preventing commercial losses, fulfillment delays, and auditing discrepancies.

## 2. Core Business Entities & Language (Ubiquitous Language)
* **Product:** An item available for sale, characterized by a unique identifier, name, unit price, stock quantity, and category.
* **Category:** A classification grouping for products.
* **Sale:** A completed commercial transaction recording the total amount and operator details.
* **Sale Item:** An individual line within a sale linking a product, its frozen unit price, and the purchased quantity.
* **User:** An internal system operator authenticated with a specific role (`admin` or `seller`).
