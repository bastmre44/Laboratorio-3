# Laboratory 3 - APIs  
Web Systems and Technologies  
Universidad del Valle de Guatemala  

## 📌 Description

This laboratory focuses on practicing REST API consumption and documentation using Postman and HTTPie.

The selected API for this project is **DummyJSON**.

Base URL:  
https://dummyjson.com

---

## 🛠 Tools Used

- Postman
- HTTPie
- Git
- GitHub

---

## 📂 Repository Contents

This repository includes:

- Happy Path Postman Collection
- Error Cases Postman Collection
- Real Request Postman Collection
- Postman Environment file
- httpie-commands.md
- API_ONBOARDING_REPORT.md
- README.md

---

## 🔍 Postman Implementation

A Postman environment was configured with the following variables:

- baseURL
- resource
- id
- query
- apikey

Three collections were created:

### 1️⃣ Happy Path
Includes:
- Main resource listing
- Detail by ID
- Search
- Advanced filtering
- Pagination
- Second resource

### 2️⃣ Error Cases
Includes:
- 404 Not Found
- 400 Bad Request
- 401 Unauthorized
- Authorization behavior case

### 3️⃣ Real Request
Includes CRUD operations:
- POST (Create)
- PUT (Update)
- PATCH (Partial Update)
- DELETE (Delete)

---

##  HTTPie

A file named `httpie-commands.md` contains at least 10 commands equivalent to the Postman tests.

It includes:
- Use of environment variables via `export`
- Custom headers
- Successful and failed requests
- Authentication cases

---

##  Documentation

The file `API_ONBOARDING_REPORT.txt` contains:

- API summary (name, base URL, authentication type, rate limit)
- Endpoints documentation table
- Evidence of successful and failed responses
- Technical observations

---


##  Notes

DummyJSON follows REST principles and supports CRUD operations.  
Authentication is required only for protected endpoints.  
The API is suitable for testing and educational purposes.