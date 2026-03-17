```markdown
# 🚀 FastAPI –  Assignment 5 (Search, Sort & Pagination)

This project demonstrates implementation of **real-world API features** using FastAPI such as:

-  Product Search  
-  Sorting Data  
-  Pagination  
-  Combined Smart Browse Endpoint  
-  Orders Search & Pagination  

---

##  Tech Stack

- Python
- FastAPI
- Uvicorn
- Swagger UI

---

##  How to Run the Project

### Step 1 — Rename the file
```

main_day6.py → main.py

```

### Step 2 — Install dependencies
```

pip install fastapi uvicorn

```

### Step 3 — Run FastAPI Server
```

uvicorn main:app --reload

```

### Step 4 — Open Swagger UI
```

[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

```

---

## 📚 Implemented API Endpoints

### 🔍 Search Products
```

GET /products/search?keyword=mouse

```
✔ Case-insensitive search  
✔ Returns friendly message if no product found  

---

### ↕️ Sort Products
```

GET /products/sort?sort_by=price&order=asc

```

Sorting Options:

- `price asc`
- `price desc`
- `name asc`
- `name desc`

---

### 📄 Products Pagination
```

GET /products/page?page=1&limit=2

```

✔ Displays limited products per page  
✔ Returns total pages  

---

### 📦 Search Orders
```

GET /orders/search?customer_name=rahul

```

✔ Case-insensitive search  
✔ Returns all matching orders  

---

### 🗂️ Sort by Category then Price
```

GET /products/sort-by-category

```

✔ Categories sorted alphabetically  
✔ Products sorted by price within category  

---

### 🧠 Smart Browse Endpoint  
(Search + Sort + Pagination Combined)

```

GET /products/browse?keyword=e&sort_by=price&order=asc&page=1&limit=2

```

✔ Optional Query Parameters  
- keyword  
- sort_by  
- order  
- page  
- limit  

---

### ⭐ Bonus — Orders Pagination
```

GET /orders/page?page=1&limit=3

```

✔ Browse large order lists easily  



---

