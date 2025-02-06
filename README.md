# API Testing with Postman for Contact List Application
 
## Project Overview
This project involves creating a comprehensive API testing suite for a Contact List Application using Postman. The goal is to ensure the API endpoints function correctly, handle both positive and negative scenarios, and validate responses. The testing will cover authentication, CRUD operations for contacts, and edge cases like invalid inputs and unauthorized access.

## Scope of Work ⚡
### 1. API Endpoints to Test:
   a. Authentication: Login, Logout<br>
   b. Contact Management: Add, Update, Get, Delete, and List Contacts<br>
   c. Negative Test Cases: Invalid inputs, missing fields, unauthorized access, etc.<br>
### 2. Tools:
   a. Postman: For API testing and automation.<br>
   b. Environment Variables: To manage dynamic data like tokens, URLs, and contact IDs.<br>
### 3. Deliverables:
   a. A Postman collection with all test cases.<br>
   b. Documentation of test scenarios and results.<br>
   c. Environment setup instructions.<br>

## Test Scenarios
### 1. Authentication
#### a. Login:
   i. Request: POST /users/login<br>
   ii. Test Cases:<br>
       - Valid credentials (status code: 200, token returned).<br>
       - Invalid credentials (status code: 401, error message).<br>
#### b. Logout:
   i. Request: POST /users/logout<br>
   ii. Test Cases:<br>
       - Valid token (status code: 200, success message).<br>
       - Invalid token (status code: 401, error message).<br>
### 2. Contact Management
#### a. Add Contact:
   i. Request: POST /contacts<br>
   ii. Test Cases:<br>
       - Valid contact data (status code: 201, contact added).<br>
       - Missing required fields (status code: 400, error message).<br>
       - Invalid email format (status code: 400, error message).<br>
#### b. Get Contact:
   i. Request: GET /contacts/:contactId<br>
   ii. Test Cases:<br>
       - Valid contact ID (status code: 200, contact details returned).<br>
       - Invalid contact ID (status code: 404, error message).<br>


