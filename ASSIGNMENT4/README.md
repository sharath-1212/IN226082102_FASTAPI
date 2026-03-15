#  FastAPI Cart System – Assignment 4

This project is a simple Shopping Cart API built using **FastAPI**.  
It demonstrates real-world cart operations like adding products, viewing cart, updating quantity, removing items, and checkout flow.

---

##  Features

- Add items to cart  
- View cart details and total price  
- Update quantity of existing products  
- Remove products from cart  
- Checkout and generate orders  
- Proper error handling (out-of-stock, invalid product, empty cart)

---

##  Tech Stack

- Python  
- FastAPI  
- Uvicorn  
- Swagger UI  

---

##  How to Run

```bash
pip install fastapi uvicorn
uvicorn main:app --reload
```

Open browser and go to:

```
http://127.0.0.1:8000/docs
```

---

##  API Endpoints

### Cart APIs
- `POST /cart/add` → Add product  
- `GET /cart` → View cart  
- `DELETE /cart/{product_id}` → Remove product  
- `POST /cart/checkout` → Checkout  

### Order APIs
- `GET /orders` → View all orders  

---

