## How does api work
You must login to get started. If you do not login, you will be notified that you are not authorized.

For login you go to to this path http://13.232.70.77/api/v1/login. The POST method is used. Input the username and password, then will be created token.
```bash
Without a token you will not be able to create objects in the future.
```
If you follow this path http://13.232.70.77/api/v1/logout and use GET method, your token will be deleted and the session will end. You will be unauthorized.
