# REST API Testing with Postman – Reqres API

🔗 This project showcases REST API testing using Postman with the dummy API service Reqres (https://reqres.in). As a QA beginner, I focused on learning how to structure API tests and write assertions for real-world endpoints.

---

## 🧪 What I Did

- Tested GET, POST, PUT, DELETE endpoints on Reqres
- Used Postman’s **Tests** tab to write validation scripts
- Added negative test cases (invalid email, missing fields)
- Exported a full Postman collection with tests and documentation

---

## 🛠 Tools Used

- Postman
- JavaScript (for writing tests in Postman)
- Reqres API (free public dummy API)

---

## 🔍 Key Tests Written

- `GET /users?page=2` – Verify response code = 200 and data array length > 0
- `POST /register` – Send valid body and check token returned
- `POST /login` – Negative test: empty password → expect error
- `DELETE /users/2` – Confirm status = 204

---

## ✅ Sample Assertion Script (Postman)

```javascript
pm.test(\"Status code is 200\", function () {
  pm.response.to.have.status(200);
});
