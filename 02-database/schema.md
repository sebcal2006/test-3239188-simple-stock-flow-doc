# Database Schema — Simple Stock Flow

## 1. Engine & Schema Configuration
* **Database Engine:** PostgreSQL 16
* **Schema:** `sales`
* **Naming Convention:** Singular table names (`product`, `category`, `sale`, `sale_item`, `user`) aligned with governance conventions.

## 2. Core Tables
* **`category`:** Defines product classification categories.
* **`product`:** Stores inventory items, unit prices, and stock counts linked to categories.
* **`user`:** Manages internal operators with specific roles (`admin` or `seller`).
* **`sale`:** Records commercial transactions with immutable headers.
* **`sale_item`:** Stores individual line items per sale, capturing frozen prices and quantities.
