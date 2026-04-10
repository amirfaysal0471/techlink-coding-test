# Techlink Coding Test - Solutions

This repository contains the completed tasks for the Techlink coding evaluation. Below is a summary of the problems addressed and the solutions implemented.

## Solutions

### 1. About Us Page and Navigation
**Requirement:** Add an “About Us” option to the navigation bar and display the content when clicked.
- **Solution:** 
  - Added a new NavLink for "About Us" in the Header.jsx component.
  - Defined the /about route in main.jsx and linked it to the existing About component.
  - Verified that users can now navigate to the About Us page directly from the header.

### 2. Frontend–Backend Connection Fix
**Requirement:** Fix the missing line in the backend to enable the API connection.
- **Solution:** 
  - Identified that the router was imported but not mounted as middleware in server/index.js.
  - Added app.use("/api", router); to the Express application.
  - This fixed the connection, as all frontend API calls are prefixed with /api.

### 3. Best Sellers Section Update (Home Page)
**Requirement:** Copy the products listed under “Top Brands” and display them in the “Best Sellers” section.
- **Solution:** 
  - Refactored client/src/components/GenInfo.jsx by moving the brand data array to a shared scope (top-level constant).
  - Renamed the variable to brandData for clarity.
  - Updated both Brands (Top Brands) and BestSellers components to use the same brandData set.

## Technology Stack
- Frontend: React, Vite, Tailwind CSS, React Router.
- Backend: Node.js, Express, MongoDB/Mongoose.

## How to Run Locally

### 1. Prerequisites
- Node.js installed.
- MongoDB running locally.

### 2. Setup
- Server:
  ```bash
  cd server
  npm install
  # Create a .env file with MONGO_URI and PORT
  npm start
  ```
- Client:
  ```bash
  cd client
  npm install
  npm start
  ```

---
