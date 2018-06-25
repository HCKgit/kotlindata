# kotlindata
another sucessful spring boot2 example with gradle

From the article: https://www.callicoder.com/kotlin-spring-boot-mysql-jpa-hibernate-rest-api-tutorial/

Create the database first (the one one the connection url in application.properties)

#Testing commands

## 1. Add an article
curl -i -H "Content-Type: application/json" -X POST \
-d '{"title": "How to learn Spring framework", "content": "Resources to learn Spring framework"}' \
http://localhost:8080/api/articles

## 2. Get al articles
curl -i -H 'Accept: application/json' http://localhost:8080/api/articles

## 3. Get article 1
curl -i -H 'Accept: application/json' http://localhost:8080/api/articles/1

## 4. Edit article 1
curl -i -H "Content-Type: application/json" -X PUT \
-d '{"title": "Learning Spring Boot", "content": "Some resources to learn Spring Boot"}' \
http://localhost:8080/api/articles/1

## 5. Delete article 1
curl -i -X DELETE http://localhost:8080/api/articles/1
