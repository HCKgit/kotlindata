# kotlindata
spring boot 2, Kotlin, gradle, intelliJ, mysql

project original creation from the command:

    $ curl https://start.spring.io/starter.zip -d type=gradle-project -d language=kotlin -d style=web,jpa,mysql -d packageName=kotlin-data -d name=sb-kotdata -o sb-kotdatav.zip

From the article: https://www.callicoder.com/kotlin-spring-boot-mysql-jpa-hibernate-rest-api-tutorial/

Create the database first (the one one the connection url in application.properties) [kotlin_demo_app]

# Testing commands

## 1. Add an article
    curl -i -H "Content-Type: application/json" -X POST \
    -d '{"title": "How to learn Spring framework", "content": "Resources to learn Spring framework"}' \
    http://localhost:8080/api/articles

## 2. Get all articles
    curl -i -H 'Accept: application/json' http://localhost:8080/api/articles

## 3. Get article 1
    curl -i -H 'Accept: application/json' http://localhost:8080/api/articles/1

## 4. Edit article 1
    curl -i -H "Content-Type: application/json" -X PUT \
    -d '{"title": "Learning Spring Boot", "content": "Some resources to learn Spring Boot"}' \
    http://localhost:8080/api/articles/1

## 5. Delete article 1
    curl -i -X DELETE http://localhost:8080/api/articles/1
