# DemoAPI — GitHub API Testing using Postman

## 🔎 Project Overview  
This repository contains API test cases (written for Postman) to test various endpoints of the GitHub REST API.  
It helps verify correctness of responses, status codes, and structure of returned data when interacting with GitHub API (e.g. user info, repo creation/deletion, etc.).

## 🧰 Tools & Technologies  
- Postman (for API testing)  
- JSON (for request/response payloads)  
- (Optional) GitHub — for versioning the test cases  


## ✅ What’s Covered / Test Scenarios  
- Validate GET user API (e.g. fetch user info)  
- Validate GET repository API  
- Validate Create repository API (if implemented)  
- Validate Delete repository API (if implemented)  
- Validate response status codes, response body structure, necessary headers  

(Add more test cases or details as you expand the project.)

## 🚀 How to Use / Run the Tests  
1. Import the Postman collection (if exported) into Postman.  
2. Configure the required environment or variables (e.g. GitHub personal access token, base URL).  
3. Run the collection.  
4. Review results — check status codes, response body, whether tests passed.  

## 📄 Sample Test Script (in Postman)  
```js
pm.test("Status code is 200", function () {
  pm.response.to.have.status(200);
});
pm.test("Response body has login field", function () {
  const data = pm.response.json();
  pm.expect(data).to.have.property("login");
});
