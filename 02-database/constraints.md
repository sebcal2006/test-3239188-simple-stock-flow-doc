# Database Constraints & Invariants — Simple Stock Flow

To guarantee absolute data integrity, critical business rules are enforced directly at the database engine level (`motor`) rather than relying solely on application-layer logic:

* **Non-Negative Stock (`stock >= 0`):** Enforced via a native PostgreSQL check constraint on the `product` table. This ensures that even direct database updates or concurrent transactions cannot push inventory levels below zero.
* **Positive Unit Prices:** Prices for products and recorded sale items must strictly be greater than zero (`price > 0`).
* **Foreign Key Integrity:** Strict referential integrity rules link `sale_item` to `sale` and `product`, as well as `product` to `category`, preventing orphan records.
