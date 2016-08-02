# ng2-ui-auth-example
To run first install rethinkdb on your localhost (http://rethinkdb.com/docs/install/)
if you're on windows it's just an exe file you need to run (no system files changes, no messy installer/uninstaller).

To create a google client id & secret you need to login to console.developers.google.com go to "credentials" create a new "OAuth Client ID" -> "Web Application" -> authorize your domain or "http://localhost:port" (if you use ionic2 the ionic port too) and then you get a "Client secret" for the server-side and a "Client ID" for the UI side.

to start the server
```
1) modify server/src/config.ts to include your google "Client secret"
2) run rethinkdb database
3) npm run server
```
to start the browser client first start the server and then:
```
1) modify client/src/bootstrap.ts to include your google "Client ID"
2) npm run client
3) start your browser in localhost:3000
```
to start the ionic client first start the server and then:
```
1) modify ionic2/app/config.ts to include your google "Client ID"
2) npm run ionic2
3) choose address and it will open the browser for you
```

Notice!
The expected result after login is two lines that look as follows:
```
~~~ Hello <user name if a google login / email if manual> ~~~

Unauthorized
```
The fist line shows the usage of jwtHttp in order to retrieve the data and the second line shows that a plain http call fails
