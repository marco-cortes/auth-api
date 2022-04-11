# My AUTH API with NODE JS & EXPRESS

## ENDPOINTS:

- /api/auth/new
  * this endpoint it's for create a new user
  * requires name, email and password
  * if done successfully, the body response will return a JSON 
    ~~~
    {
     name:user_name
     uid:user_id
     token:jwt
    }
    ~~~
- /api/auth/renew
- /api/auth/validate
  * requires a JWT
- /api/auth/
  * requires email and password
