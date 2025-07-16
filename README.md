
# 🛒 E-Commerce Web Application

An interactive and database-integrated full-stack eCommerce platform developed as part of the **DBS Course Project**. This application allows users and sellers to interact in a secure marketplace with real-time product listings, address management, cart functionality, reviews, and order processing.

---

## 📁 Project Structure

```bash
.
├── backend/                  # Node.js + Express API with Oracle DB
│   ├── controllers/          # API logic (auth, products, reviews, orders, etc.)
│   ├── db_config/            # Table creation/drop scripts
│   ├── middlewares/          # Authentication with JWT
│   └── app.js                # Entry point
└── frontend/ecom_frontend/   # React + TailwindCSS SPA
    ├── src/components/       # Reusable React components
    ├── src/pages/            # Page-level views
    ├── index.html, etc.      # Config files
```

---

## 🧠 Features Overview

### 🔐 Authentication

-   JWT-based login & signup system for:
    
    -   **Sellers**
        
    -   **Buyers**
        
-   Role-specific dashboards and access control
    

### 🛍️ Product Management

-   Sellers can:
    
    -   Add products with images, price, and category
        
    -   View products by seller
        
-   Users can:
    
    -   Browse by category
        
    -   View product details
        
    -   Add to cart
        

### 🧾 Orders & Transactions

-   Users can:
    
    -   Initiate orders and checkout
        
    -   View order confirmation and history
        
    -   Get complete address + product summary
        

### 🌍 Address Management

-   Users and sellers can add addresses from a dropdown of **Indian states**
    
-   Oracle DB constraints ensure only valid states
    

### ⭐ Reviews System

-   Buyers can add star-based reviews (0–5) with text
    
-   View reviews per product
    

---

## 🧪 Tech Stack

| Layer | Technology |
| --- | --- |
| Frontend | React, TailwindCSS, DaisyUI |
| Backend | Node.js, Express.js |
| Database | Oracle SQL |
| Auth | JWT |
| Styling | #990011 (Primary), #FCF6F5 (Accent) |

---

## 🚀 How to Run

### 🔧 Backend

```bash
cd backend
npm install
# Add your Oracle DB credentials in .env
node app.js
```

### 🌐 Frontend

```bash
cd frontend/ecom_frontend
npm install
npm run dev
```

---

## 📌 Notable Design Highlights

-   🔄 **Dynamic Image Upload** with `multer`
    
-   🎨 **Carousel Banner** on homepage
    
-   📋 **Modular Forms** for user/seller signup, login, and address inputs
    
-   🧩 **Atomic Component Design** for reusability
    
-   ⚠️ **Validations** on forms and ratings
    
-   🧹 **Clear Buttons** and resets on product forms
    
-   🧾 **Secure token-based route protection**
    

---

## 🧱 Oracle Database Schema

Key Tables:

-   `user_table`, `seller`, `product`, `review_table`
    
-   `bought`, `reviews`, `add_to_cart`, `lives`, `address`
    

Run table creation:

```bash
node backend/db_config/init_functions.js
```

---

## 🧪 Sample APIs

-   `POST /user/signup` → Register new user
    
-   `POST /seller/:seller_id/addproduct` → Add product
    
-   `GET /category/:category` → Products by category
    
-   `POST /user/:user_id/:product_id/addreview` → Add a review
    
-   `GET /user/:user_id/history` → Order history
    

---

## 🧑‍💻 Contributors

-   **Abhishek Jayanth Holla**
    

    

---

## 📚 Future Scope

-   Add Razorpay/Stripe integration for real payments
    
-   Product stock management
    
-   Wishlist and cart enhancements
    
-   Admin dashboard
    

---
