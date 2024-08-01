Тестовое задание для "Лаборатория Интернет"

# User REST API

API поддерживает следующие методы:

POST /register - Создание нового пользователя
POST /login - Авторизация пользователя
PUT /user/{id} - Обновление информации пользователя
DELETE /user/{id} - Удаление пользователя
GET /user/{id} - Получение информации о пользователе
## Endpoints

### Create User
- **URL**: `/register`
- **Method**: `POST`
- **Data Params**:
  {
    "name": "Lena",
    "email": "lalla@example.com",
    "password": "password123"
  }
- **Success Response**:
- Code: 201 Created
- Content:

{
"success": true
}
- **Error Response**:
- Code: 400 Bad Request
- Content:

{
"error": "Invalid JSON input"
}
 
### Update User
- **URL**: /user/{id}
- **Method**: PUT
- **Data Params**:

{
"name": "New Name",
"email": "newemail@example.com",
"password": "newpassword"
}
- **Success Response**:
- Code: 200 OK
- Content:

{
"success": "User updated successfully"
}

- **Error Response**:
- Code: 400 Bad Request
- Content:

{
"error": "Invalid JSON input"
}
- Code: 404 Not Found
- Content:

{
"error": "User not found"
}
### Delete User
URL: /user/{id}
Method: DELETE
Success Response:
Code: 200 OK
Content:

{
"success": "User deleted successfully"
}
Error Response:
Code: 404 Not Found
Content:

{
"error": "User not found"
}
### Get User Info
- **URL**: /user/{id}
- **Method**: GET
- **Success Response**:
- Code: 200 OK
- Content:

{
"user": {
"id": 1,
"name": "Lena",
"email": "lalla@example.com"
}
}
- **Error Response**:
- Code: 404 Not Found
- Content:

{
"error": "User not found"
}
### User Login
- **URL**: /login
- **Method**: POST
- **Data Params**:

{
"email": "lalla@example.com",
"password": "password123"
}
- **Success Response**:
- Code: 200 OK
- Content:
{
"user": {
"id": 1,
"name": "Lena",
"email": "lalla@example.com"
}
}
- **Error Response**:
- Code: 401 Unauthorized
- Content:

{
"error": "Invalid credentials"
}
