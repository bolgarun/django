## Authorization

You must login to get started. If you don't login, you will be notified that you are not authorized.
```bash
Use POST method
```
Follow this path http://13.232.70.77/api/v1/login.

Replace the fields in parameters "yourusername" and "yourpassword" on your own username and password:
```bash
                       {"username": "yourusername", "password": "yourpassword"}

                        Exampl: {"username": "sam", "password": "Sport2100"}
```
After using the POST method, the above URL and parameters (yours username and password) will be created token.
A token is a secret key without is impossible to view, create, edit or delete objects.
```bash
                       Exampl:  Token 092e00e4893d42cce7dbfddfc3a2f9e9508743d3
```

## Unauthorization
```bash
Use GET method
```
If you follow this path http://13.232.70.77/api/v1/logout and use GET method, your token will be deleted and the session will end. You will be unauthorized.
