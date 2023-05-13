# jwt secure your api..


## create token

* after creating token follow this steps:


1. client: after user login send user basic info to create token;

2. in the server side : npm jsonwebtoken;

3. import jsonwebtoken ;

4. jwt.sing(payload,secret,{(expires)})

5. return token to the client side

6. after receiving token store it either http only cookies or localStorage


7. use a general space  onAuthStateChange > AuthProviders;


## send token to server

* for sensitive api call () send authorization headers {authorization:  'bearer token' }



## verify token

1. create a function verifyJWT (middleware);

2. this function will have three params : req,res and next ;

3. first check  whether the authorization headers exists ;

4. if not send 401 status code with res.send;

5. if authorized true than get the token out of the authorization header;

6. call jwt.verify(token,secret, (error, decoded))

7. if error in callback function send 403 status code with res.send

8. if anything all  right than call next() to continue



### checked middleware email and logged email

* checked the email which routes  you call this middleware with middleware email;