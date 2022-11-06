# Endpoints specifications

You'll find here all of the endpoints for the application.

## /API/V1

### <u>User</u>

| Method | Route          | Description         | Returns     | Page      |
| ------ | -------------- | ------------------- | ----------- | --------- |
| GET    | /users/:userId | Fetch one user      | Json object | Dashboard |
| POST   | /signup        | Register user       |             |           |
| POST   | /signin        | Open user session   |             |           |
| GET    | /signout       | Logout user         |             |           |
| PATCH  | /users/:userId | Update user info    |             |           |
| DELETE | /users/:userId | Delete user account |             |           |
| POST   | /refreshToken  | Authorization token | Json object |           |

### <u>Articles</u>

| Method | Route                | Description | Returns | Page |
| ------ | -------------------- | ----------- | ------- | ---- |
| GET    | /articles            |             |         |      |
| POST   | /articles            |             |         |      |
| PATCH  | /articles/:articleId |             |         |      |
| DELETE | /articles/:articleId |             |         |      |

### <u>Categories</u>

| Method | Route                   | Description | Returns | Page |
| ------ | ----------------------- | ----------- | ------- | ---- |
| GET    | /categories             |             |         |      |
| POST   | /categories             |             |         |      |
| PATCH  | /categories/:categoryId |             |         |      |
| DELETE | /categories/:categoryId |             |         |      |
