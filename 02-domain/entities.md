# Domain Entities & Rules — Simple Stock Flow

## 1. Core Domain Aggregates & Entities
* **Product:** The primary aggregate root for inventory. Encapsulates item identity, descriptive details, pricing, stock levels, and category association.
* **Category:** Classification entity grouping products to organize the catalog logically.
* **User:** Represents system operators authenticated with distinct security roles (`admin` or `seller`).
* **Sale:** Aggregate representing a commercial transaction header, tying together the transaction timestamp, total sum, and operator details.
* **Sale Item:** Line-level entity belonging to a sale, recording the specific product sold, its quantity, and the frozen unit price at the time of purchase.

## 2. Invariants & Business Rules
* **Non-Negative Inventory Rule:** Stock levels cannot drop below zero under any circumstance, protected by underlying constraints.
* **Price Validity Rule:** Unit prices for catalog items and sale items must always be strictly greater than zero.
* **Sales Immutability Rule:** Once a sale transaction and its associated line items are completed and recorded, they become strictly immutable to guarantee accurate auditing and financial history.
