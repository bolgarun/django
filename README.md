## Authorization

You must login to get started. If you don't login, you will be notified that you are not authorized.
```bash
POST method
```
Follow this path http://13.232.70.77/api/v1/login.

Replace the fields in parameters "yourusername" and "yourpassword" on your own username and password:
```bash
                       {"username": "yourusername", "password": "yourpassword"}

                        Exampl: {"username": "sam", "password": "Sport2100"}
```
After using the POST method, the above URL and parameters (yours username and password) will be created token.
A token is a secret key without is impossible to view, create, edit or delete objects or logout.
```bash
                       Exampl:  Token 092e00e4893d42cce7dbfddfc3a2f9e9508743d3
```

## Unauthorization
```bash
GET method
```
Follow this path http://13.232.70.77/api/v1/logout

This method is not available unless you are authorized.

Going url position using the GET method and passing a Token, will be delete Token and the session will end. You will be unauthorized.


## Record and view gold rate
Using methods POST, GET, url http://13.232.70.77/api/v1/rates/gold and Token

```bash
GET method
```
GET: Read database table and return the MOST RECENT Gold rate
```bash
POST method
```
POST: to create new record with current date
Replace the field in parameter:
```bash
                        {"rate": your_rate}
                    Exampl:  {"rate": 3444.77}
```
These methods are not available to you if you are not authorized.


## Create, view, edit and delete Account
```bash
GET method
```
If GET request will accept AccountID then he return Account which you need, like:

  
