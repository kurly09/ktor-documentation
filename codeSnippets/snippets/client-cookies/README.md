# Client cookies

A sample project demonstrating how to store cookies on a client using the [HttpCookies](https://ktor.io/docs/http-cookies.html) plugin.

## Running

Before running this sample, start a server from the [session-cookie](https://github.com/ktorio/ktor-documentation/tree/%branch-name%/codeSnippets/snippets/session-cookie) example:
```bash
# macOS/Linux
./gradlew :session-cookie:run

# Windows
gradlew.bat :session-cookie:run
```
This server sends session data in the `Set-Cookie` response header after visiting the [http://0.0.0.0:8080/login](http://0.0.0.0:8080/login) page.

To run a client sample, execute the following command:

```bash
# macOS/Linux
./gradlew :client-cookies:run

# Windows
gradlew.bat :client-cookies:run
```

A client should show the following output:
```
Session ID is 123abc. Reload count is 1.
Session ID is 123abc. Reload count is 2.
Session ID is 123abc. Reload count is 3.
```
This means that a client stores session data between subsequent requests and sends cookies to a server in the `Cookie` request header.
