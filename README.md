# Capstone 2 - E-Commerce REST API 

## Description 
A REST API for managing e-commerce products using Node.js, Express, MongoDB, and Mongoose. 

## Technologies 
- Node.js 
- Express.js 
- MongoDB 
- Mongoose 
- Postman 

## Installation 
1. Clone the repository 
2. Run: npm install 
3. Create .env: PORT=5000 MONGO_URI=your_connection_string
4. Run: npm run dev ## Base URL http://localhost:5000 

## Product Endpoints 
- POST /api/products 
- GET /api/products 
- GET /api/products/:id 
- PATCH /api/products/:id 
- DELETE /api/products/:id 

## Search / Filter 
GET /api/products?category=Accessories 
GET /api/products?search=mouse 

## Testing Import/use the Postman collection: MSTCONNECT Capstone 2 API

### Create Product 
POST /api/products 

Purpose: Create a product. 

Body: { 
        "name": "Mechanical Keyboard", 
        "description": "RGB keyboard", 
        "price": 1850, 
        "category": "Accessories", 
        "stock": 12 
} 

Success: 201 Created 
Possible errors: 400 Bad Request, 500 Interal Server Error

### Get All Products 
GET /api/products

Purpose: Retrieve all products

Success: 200 OK 
Possible errors: 500 Internal Server Error

### Get Product By Id 
GET /api/products/:id

Purpose: Get a product by id

Success: 200 OK
Possible errors: 400 Bad Request, 404 Not Found, 500 Internal Server Error

### Get Product Filter/Search By 
GET /api/products/?<key>=<value>

Purpose: Get a product based on query parameter key and value pair

Success: 200 OK
Possible errors: 400 Bad Request, 404 Not Found, 500 Internal Server Error

### Update Product 
PATCH /api/products/:id

Purpose: Modify specific fields of a product by id

Body: {
    "stock": 13
}

Success: 200 OK
Possible errors: 400 Bad Request, 404 Not Found, 500 Internal Server Error

### Delete Product 
DELETE /api/products/:id

Purpose: Delete a product by id.

Success: 200 OK 
Possible errors: 400 Bad Request (invalid ID), 404 Not Found, 500 Internal Server Error