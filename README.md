# My AUTH API with NODE JS & EXPRESS
#### That is an implementation of JWT with node, express and mongodb
#### Try it on: https://marco-cortes-auth.herokuapp.com/
## ENDPOINTS:

- /api/auth/new
  * this endpoint it's for create a new user
  * type: post
  * requires name, email and password
  * if done successfully, the body response will return the next JSON:
    ~~~
    {
     ok: true,
     message: "register",
     user: {
      name: usuario.name,
      uid: usuario._id,
      token
     }
    }
    ~~~
    otherwise the response will be:
    ~~~
    {
     ok:false,
     message:"error message"
    }
    ~~~
- /api/auth/renew
  * this enpoint it's for renew the JWT
  * type: get
  * requires an JWT sent by headers
  * the response it's the same of /api/auth/new endpoint
- /api/auth/validate
  * that endpoint it's for validate a session in other api
  * type: get
  * requires an JWT sent by headers
  * only returns an "ok" true or false in a JSON
- /api/auth/
  * that endpoint it's for create a new session (login)
  * type: post
  * requires email and password
  * the response it's the same of /api/auth/new endpoint
