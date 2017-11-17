1. Setting POSTGRESQL environment in /src/main/resources/application.properties 
2. Run app with Spring Boot
3. Create account: 
```
curl -X POST \
  http://localhost:8080/api/register \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{
	"name": "Test",
	"username": "test",
	"email": "test@example.com",
	"password": "test"
}'
```
4. Get access token (by JDBC or InMemory)
```
curl -X POST \
  'http://localhost:8080/oauth/token?grant_type=password&username=admin&password=admin' \
  -H 'authorization: Basic Y2xpZW50YXBwOjEyMzQ1Ng==' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded'
```