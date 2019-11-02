## Authorization
You must login to get started. If you don't login, you will be notified that you are not authorized.
```bash
POST method
```
Follow this path http://13.232.70.77/api/v1/login.

```bash
                          {"username": "yourusername", "password": "yourpassword"}
```
Input the username and password, then will be created token.
```bash
Without a token you will not be able to create objects in the future.
```
If you follow this path http://13.232.70.77/api/v1/logout and use GET method, your token will be deleted and the session will end. You will be unauthorized.
