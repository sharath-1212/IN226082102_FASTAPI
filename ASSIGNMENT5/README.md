

```
#  FastAPI Project – Search, Sort & Pagination API

This project is developed as part of the **FastAPI Internship Training – Day 6 Assignment**.  
It demonstrates implementation of **real-world REST API features** such as searching, sorting, pagination and combining all operations into a single smart endpoint.

---

##  Features Implemented

 Product Search (Case-Insensitive)  
 Product Sorting (Price & Name)  
 Product Pagination  
 Orders Search by Customer Name  
 Multi-Level Sorting (Category → Price)  
 Smart Browse Endpoint (Search + Sort + Pagination Combined)  
 Orders Pagination (Bonus Feature)

---

##  Tech Stack

- Python  
- FastAPI  
- Uvicorn  
- Swagger UI  

---

##  How to Run the Project

### 1️ Rename the file
```

main_day6.py → main.py

```

### 2️ Install dependencies
```

pip install fastapi uvicorn

```

### 3️ Run the FastAPI server
```

uvicorn main:app --reload

```

### 4️ Open API Documentation
```

[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

```

---

##  API Endpoints Overview

###  Search Products
```

GET /products/search?keyword=mouse

```
- Performs case-insensitive keyword search  
- Returns friendly message if no results found  

---

###  Sort Products
```

GET /products/sort?sort_by=price&order=asc

```
Sorting Options:
- Price Low → High  
- Price High → Low  
- Name A → Z  
- Name Z → A  

---

###  Product Pagination
```

GET /products/page?page=1&limit=2

```
- Displays limited products per page  
- Returns total pages  

---

###  Search Orders
```

GET /orders/search?customer_name=rahul

```
- Returns all orders matching customer keyword  
- Case-insensitive search  

---

###  Sort Products by Category then Price
```

GET /products/sort-by-category

```
- Categories sorted alphabetically  
- Products sorted by price within each category  

---

###  Smart Browse Endpoint  
(Combined Search + Sort + Pagination)

```

GET /products/browse?keyword=e&sort_by=price&order=asc&page=1&limit=2

```

Optional Parameters:
- keyword  
- sort_by (price / name)  
- order (asc / desc)  
- page  
- limit  

---

###  Bonus – Orders Pagination
```

GET /orders/page?page=1&limit=3

```
- Helps browse large order datasets  

---

