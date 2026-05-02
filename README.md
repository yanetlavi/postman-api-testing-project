# 📌 Postman API Testing Project — JSONPlaceholder

This project demonstrates a complete API testing workflow using **Postman**, including:
- Environment variables  
- Dynamic variable chaining  
- Automated tests  
- Collection Runner execution  
- Negative testing  
- Real‑world CRUD test design  

The API used is **JSONPlaceholder**, a public mock API commonly used for learning and testing.

---

## 🚀 Project Overview

This collection simulates a full CRUD workflow:

1. GET all posts  
2. GET a single post (static ID)  
3. POST a new post  
4. GET the newly created post (dynamic ID)  
5. PUT update  
6. PATCH update  
7. DELETE  
8. Negative tests (invalid IDs, missing fields, invalid data)

All requests include automated tests written in JavaScript using Postman’s `pm` API.

---

## 🧪 Tests Included

Each request contains tests such as:

- Status code validation  
- Response structure validation  
- Required fields  
- Data types  
- Negative scenario validation  
- Dynamic variable usage (`postId`)  

The POST request stores the returned `id` into an environment variable:

```javascript
const json = pm.response.json();
pm.environment.set("postId", json.id);
