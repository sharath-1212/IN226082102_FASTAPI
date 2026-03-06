# FastAPI E-commerce API Assignment

This is a simple FastAPI application that demonstrates various API endpoints for an e-commerce product management system.

## Features

The API includes the following endpoints:

### Basic Endpoints
- **GET /** - Welcome message
- **GET /products** - Returns all products
- **GET /products/{product_id}** - Returns a specific product by ID

### Filtering & Search
- **GET /products/filter** - Filter products by category, max price, and stock status
- **GET /products/category/{category_name}** - Get products by category (Electronics/Stationery)
- **GET /products/instock** - Returns only in-stock products
- **GET /products/search/{keyword}** - Search products by name

### Analytics & Summary
- **GET /products/deals** - Returns cheapest and most expensive products
- **GET /store/summary** - Store statistics including product counts and categories

## Sample Data

The API uses a temporary in-memory database with 7 sample products including:
- Electronics: Wireless Mouse, USB Hub, Laptop stand, Mechanical keyboard, Webcam
- Stationery: Notebook, Pen Set

## Getting Started

### Prerequisites
- Python 3.7+
- FastAPI
- Uvicorn

### Installation
```bash
pip install fastapi uvicorn
```

### Running the Application
```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`

### API Documentation
Once running, visit:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## Example Requests

### Get all products
```
GET /products
```

### Filter Electronics under 1000
```
GET /products/filter?category=Electronics&max_price=1000
```

### Search for "mouse"
```
GET /products/search/mouse
```

### Get store summary
```
GET /store/summary
```
