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
Using methods POST, GET, PUT, DELETE, http://13.232.70.77/api/v1/accounts and Token

```bash
GET method
```
If GET request will accept AccountID then he return Account which you need, like:

http://13.232.70.77/api/v1/accounts/1 - will return an Account that has id 1

http://13.232.70.77/api/v1/accounts/2 - will return an Account that has id 2

If GET request not accept AccountID then he return all Account from database

```bash
POST method
```
POST response will send back the generated CustomerID

To create an account you need to:
* url http://13.232.70.77/api/v1/accounts
* method POST
* Token (exampl: Token 092e00e4893d42cce7dbfddfc3a2f9e9508743d3)
* and fill in the value

```bash
          Exampl value: {
                          "first_name": "Solya",
                          "last_name":"Pior",
                          "email":"oos@gmail.com",
                          "phone":"+3009080832",
                          "os":"MacOS",
                          "os_version":"11",
                          "date_of_birth":"1994-10-10"
                        }
```

```bash
PUT method
```
PUT request will accept all Account fields and will update the customer details of the matching ID

To update account you need to:
* url http://13.232.70.77/api/v1/accounts/AccountID
* method PUT
* Token (exampl: Token 092e00e4893d42cce7dbfddfc3a2f9e9508743d3)
* and fill in the value

```bash
          Exampl value: {
                          "first_name": "Poll",
                          "last_name":"Cold",
                          "email":"change@gmail.com",
                          "phone":"+3009080832",
                          "os":"MacOS",
                          "os_version":"11",
                          "date_of_birth":"1994-10-10"
                        }
```

```bash
DELETE method
```
DELETE request removes the account from the database

For delete account you need to:
* url http://13.232.70.77/api/v1/accounts/AccountID
* method DELETE
* Token (exampl: Token 092e00e4893d42cce7dbfddfc3a2f9e9508743d3)

## Create REFER FRIEND
Using methods POST, url http://13.232.70.77/api/v1/referrals and Token
```bash
POST method
```
POST request will accept all bellow fields and create a new record in database table

Using methods POST, url http://13.232.70.77/api/v1/referrals and Token
```bash
                 Exampl :  {
                               "friend_first_name": "Ala",
                               "friend_last_name":"oor",
                               "friend_email":"rops@gmail.com",
                               "friend_phone":"+3009292932"
                           }
```
