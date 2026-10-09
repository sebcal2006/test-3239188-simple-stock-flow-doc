# Functional Requirements — Simple Stock Flow

* **FR-01 (Product Catalog):** The system must maintain a product catalog (`product` table) linked to fixed categories (`category` table) with strict validation on positive unit prices and non-negative stock levels.
* **FR-02 (Immutable Sales):** Completed sales (`sale` and `sale_item` tables) must remain immutable once recorded. Prices must be frozen at the moment of the transaction.
* **FR-03 (User Authentication & Roles):** The system must authenticate internal operators (`user` table) assigned to either an `admin` or `seller` role.
