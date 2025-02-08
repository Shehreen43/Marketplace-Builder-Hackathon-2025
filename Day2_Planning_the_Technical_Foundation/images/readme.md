# E-Commerce Marketplace - Hackathon Day 2

## **Project Overview**

This project is an e-commerce marketplace designed during a hackathon. The goal of Day 2 is to transition from business requirements to technical planning and create a robust foundation for implementation. The project aims to deliver a seamless shopping experience with scalable and secure backend support.

---

## **Technical Requirements**

### **1. Frontend**

- **Purpose**: Provide a seamless and responsive user experience.
- **Pages**:
  1. **Home Page**: Highlights featured products and categories, with a promotional banner.
  2. **Product Listing Page**: Displays all available products with search, filters, and sorting functionality.
  3. **Product Details Page**: Offers detailed product information, including images, reviews, and an "Add to Cart" button.
  4. **Cart Page**: Summarizes selected items for purchase, with quantity controls and an option to proceed to checkout.
  5. **Checkout Page**: Collects user details, shipping address, and payment information.
  6. **Order Confirmation Page**: Displays the order summary, estimated delivery time, and tracking options.
  7. **Sign Up/Login Page**: Manages user authentication using **Clerk**, with secure OAuth and password reset options.
  8. **Wishlist Page**: Allows users to save products for later review or purchase.

  <img src="/images/Frontend.PNG" alt="System Architecture" width="600">


### **2. Backend**

- **Purpose**: Manage and store data dynamically using **Sanity CMS**.
- **Schemas**:
  - **Product**: Fields for name, price, stock, image, description, and category.
  - **Order**: Fields for order ID, customer details, product list, total price, and status.
  - **User** (Optional): Fields for email, password, and wishlist.

   <img src="/images/Frontend.PNG" alt="System Architecture"width="600">

### **3. Third-Party APIs**

- **Stripe**: For secure and efficient payment processing.
- **ShipEngine**: For real-time shipping updates and tracking.

 <img src="/images/API.PNG" alt="System Architecture" width="600">

---

## **System Architecture**

### **High-Level Design**

```
[Frontend (Next.js)] <--> [Sanity CMS] <--> [Third-Party APIs: Stripe, ShipEngine]
```

### **Workflows**

1. **User Registration and Login**:
   - User registers/logs in using Clerk.
   - User data is securely stored in Clerk's database.
2. **Product Browsing**:
   - Frontend dynamically fetches product data from Sanity CMS.
3. **Order Placement**:
   - Cart details and order information are sent to Sanity CMS.
   - Payment is securely processed via Stripe.
4. **Order Tracking**:
   - Shipment status is retrieved from ShipEngine API and displayed to the user.

---

## **API Requirements**

### **1. Products**

- **GET /products**
  - Fetch all available products.
  - **Response**:
    ```json
    {
      "id": 1,
      "name": "Product A",
      "price": 100,
      "stock": 50,
      "category": "Electronics"
    }
    ```

### **2. Orders**

- **POST /orders**
  - Create a new order.
  - **Payload**:
    ```json
    {
      "customerInfo": {
        "name": "John Doe",
        "email": "john@example.com"
      },
      "cartItems": [
        { "productId": 1, "quantity": 2 },
        { "productId": 2, "quantity": 1 }
      ],
      "paymentStatus": "Paid"
    }
    ```

### **3. Shipment**

- **GET /shipment/:orderId**
  - Fetch tracking updates for an order.
  - **Response**:
    ```json
    {
      "orderId": 123,
      "status": "In Transit",
      "ETA": "2 days"
    }
    ```

---

## **Tools and Technologies Used**

1. **Next.js**: Framework for building the frontend.
2. **Tailwind CSS**: Utility-first CSS framework for styling and    responsiveness.
3. **Sanity CMS**: Headless CMS for backend data management.
4. **Clerk**: Modern authentication platform for secure user management.
5. **Stripe**: Payment processing solution for seamless transactions.
6. **ShipEngine**: API for real-time shipping rates and tracking.

---
