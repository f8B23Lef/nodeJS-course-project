# nodeJS-course-project

## TASK 2.1
Write a simple **RES**T service with **CRUD** operations for User entity.
1. To create **REST** service, use **ExpressJS** (https://expressjs.com/).
The User should have the following properties (you can use **UUID** as a user identifier (**id**)):
https://imgur.com/YZnYwEz
2. Service should have the following **CRUD** operations for **User**:
    1. get user by **id**;
    1. create and update user;
    1. get auto-suggest list from *limit* users, sorted by login property and filtered by *loginSubstring* in the login property:
`getAutoSuggestUsers(loginSubstring, limit)`
    1. remove user (**soft delete** – user gets marked with *isDeleted* flag, but not removed from
the collection).
3.  Store user’s collection in the service memory (while the service is running).

To test the service **CRUD** methods, you can use **Postman** (https://www.getpostman.com/).

## TASK 2.2
Add server-side validation for create/update operations of **User** entity:
1. all fields are required;
2. login validation is required;
3. password must contain letters and numbers;
4. user’s age must be between 4 and 130.

In case of any property does not meet the validation requirements or the field is absent, return **400 (Bad Request)** and detailed error message.
For requests validation use special packages like **joi**
(https://github.com/hapijs/joi, https://www.npmjs.com/package/express-joi-validation).