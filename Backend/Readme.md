# User Registration API

## Endpoint: `/users/register`

### Description
This endpoint allows users to register by providing their personal information. It validates the input data and creates a new user in the database.

### Required Data
The following fields are required in the request body:

- `fullname`: An object containing:
  - `firstname`: A string representing the user's first name (minimum 3 characters).
  - `lastname`: A string representing the user's last name (minimum 3 characters).
- `email`: A string representing the user's email address (must be a valid email format and unique).
- `password`: A string representing the user's password (minimum 6 characters).

### Request Example
{
  "fullname": {
    "firstname": "John",
    "lastname": "Doe"
  },
  "email": "john.doe@example.com",
  "password": "securepassword"
}

### Status Codes
- `201 Created`: User successfully registered.
- `400 Bad Request`: Validation errors occurred (e.g., missing fields or invalid data).
- `409 Conflict`: Email already exists in the database.

### Notes
Ensure that the request body is formatted as JSON and that all required fields are included to avoid validation errors.

### Example Response
- `fullname`: An object containing:
  - `firstname`: A string ( minimum 3 characters).
  - `lastname`: A string ( minimum 3 characters).
- `email`: A string ( must be a valid email format and unique).
- `password`: A string ( minimum 6 characters).
- `token`: A string (JWT token).

# User Login API

## Endpoint: `/users/login`

### Description

This endpoint allows users to log in by providing their email and password. It validates the input data and returns a JWT token upon successful authentication.

### Request Body

The following fields are required in the request body, which should be formatted as JSON:

```json
{
  "email": "john.doe@example.com",
  "password": "securepassword"
}

### Example Response
- `fullname`: An object containing:
  - `firstname`: A string ( minimum 3 characters).
  - `lastname`: A string ( minimum 3 characters).
- `email`: A string ( must be a valid email format and unique).
- `password`: A string ( minimum 6 characters).
- `token`: A string (JWT token).


