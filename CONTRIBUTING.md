# QA Readiness Checklist

## What Developers Need to Ensure (QA/QC Readiness)

---

### Frontend (React):

#### Input Validations:

- **What it means:** Ensuring the user enters only valid data (e.g., no letters in a phone number field).
- **Why it matters:** Prevents bad data from reaching the backend (server/database) and helps QA test how different inputs behave.

**Example (Without input validation):**

- A user could enter `abc` in the Phone Number field.
- Or leave the Email blank.
- Or enter special characters in the Name field.

This can confuse the system or even break it!

---

#### Error Messages:

- **What it means:** Messages shown when something goes wrong (e.g., "Password is too short").
- **Why it matters:** QA checks if users are getting helpful feedback when mistakes are made.

---

#### Browser Console Logs:

- **What it means:** Developers use the `console.log()` to show outputs/errors in the browser console.
- **Why it matters:** QA uses these logs to report errors and understand frontend issues better.

---

#### Unit Testing of Components:

- **What it means:** Small tests for individual components (like buttons or forms) using testing tools like Jest.
- **Why it matters:** Finds issues early before QA starts testing the full app.

---

### Backend (Java + Spring Boot + REST APIs):

#### Logging:

- **What it means:** Server-side logs record errors, actions, or important info using tools like Log4j or SLF4J.
- **Why it matters:** QA and devs can troubleshoot backend issues easily.

---

#### Error Codes in APIs:

- **What it means:** API responses should return proper status codes (e.g., 404, 500) and messages.
- **Why it matters:** QA understands what's going wrong and where, like authentication failures.

---

#### Exception Handling:

- **What it means:** The Backend should gracefully catch and handle unexpected situations without crashing.
- **Why it matters:** QA can continue testing even if things go wrong; no white screens or server crashes.

---

#### Request Validations:

- **What it means:** Backend checks if request data is valid (e.g., price not negative).
- **Why it matters:** Helps QA ensure incorrect data gets blocked at the server level.

---

#### API Documentation:

- **What it means:** Clear documentation (e.g., using Swagger) explaining how each API works.
- **Why it matters:** QA knows exactly how to test API inputs and outputs.

---

### Database Layer:

#### Data Integrity:

- **What it means:** Enforcing rules like primary/foreign keys to keep data accurate and connected.
- **Why it matters:** QA doesn’t have to worry about duplicate or broken records.

---

#### DB Validations:

- **What it means:** Rules directly in DB (e.g., "email" should not be null).
- **Why it matters:** Ensures correctness even if validations fail in the frontend/backend.

> **Note:**
> - **Data Integrity:** Ensures data is correct, consistent, and reliable.
> - **DB Validation:** Specific DB rules like NOT NULL, UNIQUE, etc.

---

#### Sample Test Data:

- **What it means:** Dummy data in tables (users, orders, etc.) for testing purposes.
- **Why it matters:** QA saves time by not needing to create test data manually.

---

## Testing Resources You (QA) Need From Them:

### FRONT-END:

- Links to working pages/web app (weblinks)
- List of completed features/components
- Any test credentials (if login required)
- Info about input fields, expected values, validations

---

### Server:

- API documentation (Swagger or Postman collection)
- Base URLs + API Paths
- Expected request/response format
- Sample input data
- Info about error codes or response messages

---

### Database (Data layer):

- Access to test DB or SQL dump
- Table Structure (column names, data types)
- Sample test data
- Any constraints/validations set at the DB level
