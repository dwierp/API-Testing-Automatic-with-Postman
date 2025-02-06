# API Testing with Postman for Contact List Application
 
## Project Overview
This project involves creating a comprehensive API testing suite for a Contact List Application using Postman. The goal is to ensure the API endpoints function correctly, handle both positive and negative scenarios, and validate responses. The testing will cover authentication, CRUD operations for contacts, and edge cases like invalid inputs and unauthorized access.

## Scope of Work
### 1. API Endpoints to Test:
   a. Authentication: Login, Logout
   b. Contact Management: Add, Update, Get, Delete, and List Contacts
   c. Negative Test Cases: Invalid inputs, missing fields, unauthorized access, etc.
### 2. Tools:
   a. Postman: For API testing and automation.
   b. Environment Variables: To manage dynamic data like tokens, URLs, and contact IDs.
### 3. Deliverables:
   a. A Postman collection with all test cases.
   b. Documentation of test scenarios and results.
   c. Environment setup instructions.

## Test Scenarios
### 1. Authentication
a. Login:
   i. Request: POST /users/login
   ii. Test Cases:
       - Valid credentials (status code: 200, token returned).
       - Invalid credentials (status code: 401, error message).
b. Logout:
   i. Request: POST /users/logout
   ii. Test Cases:
       - Valid token (status code: 200, success message).
       - Invalid token (status code: 401, error message).
