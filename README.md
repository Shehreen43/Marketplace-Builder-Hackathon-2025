# Marketplace-Builder-Hackathon-2025 

# E-Commerce Website - Hackathon Documentation

## Day 1: Business Foundation
On Day 1, I outlined the foundation of my e-commerce business on paper. This included:
- Selecting a general e-commerce business model.
- Defining business goals and objectives.
- Structuring the data schema for **Sanity CMS** to manage products, orders, and user data.

---

## Day 2: Technical Planning & Requirements
### Project Overview
- Transitioned from business requirements to technical planning.
- Defined a scalable and secure architecture.

### Technical Requirements
#### Frontend
- Built with **Next.js** for a responsive UI.
- Integrated pages:
  - Home, Product Listing, Product Details, Cart, Checkout, Order Confirmation, Sign Up/Login, Wishlist.
- Authentication via **Clerk**.

#### Backend
- Managed via **Sanity CMS**.
- Schema for products, orders, and users.

#### Third-Party APIs
- **Stripe** for payments.
- **ShipEngine** for shipment tracking.

---

## Day 3: API Integration & Data Migration
- Integrated external product API using **Axios**.
- Migrated product data to **Sanity CMS**.
- Displayed data dynamically using **GROQ queries** in Next.js.
- Ensured type safety with **Typegen & Zod schemas**.

---

## Day 4: Dynamic Frontend Components
Developed dynamic, reusable UI components:
- **Product Listing Component**
- **Product Detail Component**
- **Category Component**
- **Search Bar**
- **Cart Component**
- **Wishlist Component**
- **Checkout Flow Component**
- **User Register/Login (Clerk)**

---

## Day 5: Testing & Optimization
### Functional Testing
- Verified product listing, search, and cart operations.
- Ensured dynamic routing for product pages.

### Error Handling & Security Testing
- API response testing via **Postman**.
- Secure API key management.

### Performance Optimization
- Improved accessibility, SEO, and load times.
- Ensured cross-browser and cross-device compatibility.

---

## Day 6: Deployment & Performance Testing

### Completed Successfully
Day 6 was successfully completed with the deployment of the e-commerce website on **Vercel**. The website is now live and fully functional with all key features implemented.
### Deployment Platform
- **Platform:** Vercel
- **Deployment URL:** [Insert Deployed Link]

### Environment Variables Configuration
Stored securely in `.env.local` and Vercel’s settings:
```env
NEXT_PUBLIC_SANITY_PROJECT_ID=""
NEXT_PUBLIC_SANITY_DATASET=""
NEXT_PUBLIC_BASE_URL=""
SANITY_API_TOKEN=""
SANITY_STUDIO_PROJECT_ID=""
SANITY_STUDIO_DATASET=""
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=""
CLERK_SECRET_KEY=""
SANITY_API_READ_TOKEN=""
STRIPE_SECRET_KEY=""
```

### Performance Testing
- Conducted via **GTmetrix**.
- **Key Fixes:**
  - Optimized images.
  - Minified CSS & JS.
  - Implemented lazy loading.
  - Reduced third-party requests.

### Test Case Report
| Test Case ID | Test Case Description | Test Steps | Expected Result | Actual Result | Status | Severity Level | Assigned To | Remarks |
|-------------|----------------------|------------|----------------|--------------|--------|---------------|------------|---------|
| TC001 | Validate Product Listing | Load product page and check if products are displayed | Products should be listed correctly | Products displayed as expected | Passed | Low | Frontend Dev | N/A |
| TC002 | Filter Products by Category | Select a category filter and check results | Only products from selected category should be shown | Filtered products displayed correctly | Passed | Medium | Frontend Dev | N/A |
| TC003 | Search Functionality | Enter a keyword and check the search results | Relevant products should be displayed | Some irrelevant products shown | Failed | High | Frontend Dev | Fix search algorithm |
| TC004 | Add Product to Cart | Click 'Add to Cart' button for a product | Product should appear in cart | Product added to cart successfully | Passed | Low | Frontend Dev | N/A |
| TC005 | Update Cart Quantity | Increase/decrease quantity in cart | Updated quantity should reflect correctly | Quantity updated correctly | Passed | Low | Frontend Dev | N/A |
| TC006 | Remove Product from Cart | Click 'Remove' on a cart item | Product should be removed from cart | Item removed successfully | Passed | Low | Frontend Dev | N/A |
| TC007 | Dynamic Routing | Click on a product to open its details page | Product details should load correctly | Product page loaded with correct details | Passed | Medium | Frontend Dev | N/A |
| TC008 | API Response Handling | Simulate API failure and check error handling | Error message should appear | Proper error message displayed | Passed | High | Backend Dev | N/A |
| TC009 | Fallback UI for Empty Data | Check UI when no products are available | 'No items found' message should appear | Message displayed correctly | Passed | Low | Frontend Dev | N/A |
| TC010 | Image Optimization | Check image sizes and loading time | Images should load quickly with reduced size | Optimized images loaded correctly | Passed | Medium | Frontend Dev | N/A |
| TC011 | Lazy Loading | Scroll down and check lazy loading | Images/assets should load only when needed | Lazy loading works as expected | Passed | Medium | Frontend Dev | N/A |
| TC012 | Cross-Browser Testing | Check functionality on Chrome, Firefox, Safari, Edge | All browsers should display correctly | Minor UI issue on Safari | Failed | Medium | Frontend Dev | Fix Safari-specific UI issues |
| TC013 | Security Testing - Input Validation | Enter invalid email and phone | Should not allow incorrect input | Validation errors displayed correctly | Passed | High | Frontend Dev | N/A |
| TC014 | Secure API Communication | Check if API requests are using HTTPS | Requests should be over HTTPS | All API calls are secure | Passed | High | Backend Dev | N/A |
| TC015 | User Acceptance Testing (UAT) | Simulate real-world usage like browsing, adding to cart, and checkout | Everything should work smoothly | Minor UI issue in checkout | Failed | Medium | Frontend Dev | Fix checkout UI glitch |

### Final Checklist
- [x] Deployment to Vercel completed  
- [x] Environment variables securely configured  
- [x] Performance testing on GTmetrix completed  
- [x] Test case report documented  
- [x] Project repository structured with README.md  

---

## Conclusion
The e-commerce website was successfully developed and deployed, with secure credentials, optimized performance, and comprehensive testing. All relevant reports and documentation are maintained in the GitHub repository for future reference.

