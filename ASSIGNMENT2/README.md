#  FastAPI Assignment 2

This project contains **practice tasks for learning FastAPI concepts** such as:

-  GET Endpoints  
-  Query Parameters  
-  POST Requests  
-  Pydantic Validation  
-  Business Logic Implementation  

---

## 📂 Project Setup

### ▶️ Run the FastAPI Server

```bash
uvicorn main:app --reload
```

Open Swagger UI for testing:

```
http://127.0.0.1:8000/docs
```

---

##  Tasks Overview

###  Q1 — Filter Products by Minimum Price
- Add query parameter `min_price` to `/products/filter`
- Should work together with existing filters like `category` and `max_price`

Example:
```
/products/filter?min_price=400
```

---

###  Q2 — Get Only Product Price
Create endpoint:

```
GET /products/{product_id}/price
```

✔ Return only:
- `name`
- `price`

 If product not found:
```json
{"error": "Product not found"}
```

---

###  Q3 — Customer Feedback API
Create **Pydantic Model**:

- `customer_name` → string (min 2 chars)
- `product_id` → int (>0)
- `rating` → int (1–5)
- `comment` → optional (max 300 chars)

Endpoint:

```
POST /feedback
```

Response should include:
- confirmation message
- saved feedback
- total feedback count

---

###  Q4 — Product Summary Dashboard
Create endpoint:

```
GET /products/summary
```

Return:

- total_products  
- in_stock_count  
- out_of_stock_count  
- most_expensive (name & price)  
- cheapest (name & price)  
- categories list  

---

###  Q5 — Bulk Order Processing
Create models:

- `OrderItem`
- `BulkOrder`

Endpoint:

```
POST /orders/bulk
```

Logic:

- Validate each item
- If product not found / out of stock → add to **failed list**
- Valid orders → add to **confirmed list**
- Calculate **grand total**

---

##  Bonus Task — Order Status Tracker

Enhance existing order system:

- New orders should start with status → `"pending"`
- Create endpoint:

```
GET /orders/{order_id}
```

- Create endpoint:

```
PATCH /orders/{order_id}/confirm
```

✔ Changes status → `"confirmed"`

---
