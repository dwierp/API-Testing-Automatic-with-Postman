# API Testing with Postman for Contact List Application
 
## Project Overview
This project involves creating a comprehensive API testing suite for a Contact List Application using Postman. The goal is to ensure the API endpoints function correctly, handle both positive and negative scenarios, and validate responses. The testing will cover authentication, CRUD operations for contacts, and edge cases like invalid inputs and unauthorized access.

## Scope of Work ⚡
### 1. API Endpoints to Test:
- Authentication: Login, Logout<br>
- Contact Management: Add, Update, Get, Delete, and List Contacts<br>
- Negative Test Cases: Invalid inputs, missing fields, unauthorized access, etc.<br>
### 2. Tools:
- Postman: For API testing and automation.<br>
- Environment Variables: To manage dynamic data like tokens, URLs, and contact IDs.<br>
### 3. Deliverables:
- A Postman collection with all test cases.<br>
- Documentation of test scenarios and results.<br>
- Environment setup instructions.<br>

## Test Scenarios
### 1. Authentication
#### a. Login:
- Request: POST /users/login<br>
- Test Cases:<br>
    - Valid credentials (status code: 200, token returned).<br>
    - Invalid credentials (status code: 401, error message).<br>
#### b. Logout:
- Request: POST /users/logout<br>
- Test Cases:<br>
  - Valid token (status code: 200, success message).<br>
  - Invalid token (status code: 401, error message).<br>
### 2. Contact Management
#### a. Add Contact:
- Request: POST /contacts<br>
- Test Cases:<br>
  - Valid contact data (status code: 201, contact added).<br>
  - Missing required fields (status code: 400, error message).<br>
  - Invalid email format (status code: 400, error message).<br>
#### b. Get Contact:
- Request: GET /contacts/:contactId<br>
- Test Cases:<br>
  - Valid contact ID (status code: 200, contact details returned).<br>
  - Invalid contact ID (status code: 404, error message).<br>
#### c. Update Contact:
- Request: PUT /contacts/:contactId<br>
- Test Cases:<br>
  - Valid update data (status code: 200, contact updated).<br>
  - Invalid email format (status code: 400, error message).<br>
#### d. Delete Contact:
- Request: DELETE /contacts/:contactId<br>
- Test Cases:<br>
   - Valid contact ID (status code: 200, success message).<br>
   - Invalid contact ID (status code: 404, error message).<br>
#### e. List Contacts:
- Request: GET /contacts<br>
- Test Cases:<br>
   - Valid token (status code: 200, list of contacts returned).<br>
   - Invalid token (status code: 401, error message).<br>
### 3. Negative Test Cases
- Unauthorized Access:<br>
   - Attempt to access protected endpoints without a token.<br>
- Invalid Data:<br>
   - Test with missing fields, invalid email, or excessively long fields.<br>
- Non-Existent Resources:<br>
   - Attempt to access or modify a contact that does not exist.<br>

## Postman Collection Structure
The Postman collection will be organized into folders for better readability and maintenance:
### 1. Basic Endpoints Test:
- Login<br>
- Get Contact List<br>
- Add Contact<br>
- Update Contact<br>
- Get Contact<br>
- Delete Contact<br>
- Logout<br>
### 2. Negative Case:
- Get Contact List - Unauthorized<br>
- Get Contact - Not Found<br>
- Add Contact - Missing Required Field<br>
- Add Contact - Last Name Too Long<br>
- Update Contact - Invalid Email<br>
- Delete Contact - Not Found<br>

## Environment Variables
The following environment variables will be used:
- url: Base URL of the API (e.g., https://api.example.com).<br>
- email: User email for login.<br>
- password: User password for login.<br>
- token: Authentication token returned after login.<br>
- contactId: ID of the contact created during testing.<br>

## Test Scripts
### Each request will include test scripts to validate:
- Status Codes: Ensure the correct HTTP status code is returned.<br>
- Response Body: Validate the presence of specific data or error messages.<br>
- Response Time: Ensure the API responds within an acceptable time frame (e.g., less than 3000ms).<br>

### Example Test Script:

javascript
Copy
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Contact is added", function () {
    pm.expect(pm.response.text()).to.include("jdoe@fake.com");
});

## Deliverables
### 1. Postman Collection:
- Exported as a JSON file.<br>
- Includes all test cases and scripts.<br>
### 2. Environment File:
- Exported as a JSON file.<br>
- Contains predefined variables for testing.<br>
### 3. Test Documentation:
- List of all test scenarios.<br>
- Expected results and actual results.<br>
- Screenshots of test runs (optional).<br>
### 4. Instructions:
- How to import and run the collection in Postman.<br>
- How to set up the environment.<br>
## Timeline
- <b>Day 1-2:</b> Set up Postman collection and environment.<br>
- <b>Day 3-4:</b> Write test scripts for positive scenarios.<br>
- <b>Day 5-6:</b> Write test scripts for negative scenarios.<br>
- <b>Day 7:</b> Finalize documentation and deliver the project.<br>





- Item pertama
    - Sub-item 1
    - Sub-item 2
