# student-crud-app
### Things todo list:
1. Clone this repository: `git clone https://github.com/hendisantika/student-crud-app.git`
2. Navigate to the folder: `cd student-crud-app`
3. Change your MySQL Credentials with your own in application.properties
4. Run the application: `mvn clean spring-boot:run`
5. Import the POSTMAN Collection.
### Image Screen shots
Add New Student
![Add New Student](img/add.png "Add New Student")
```shell
curl --location --request POST 'localhost:8080/api/students' \
--header 'Content-Type: application/json' \
--data-raw '{
    "firstName" : "Muhammad Rahmat",
    "lastName": "Muhaimin",
    "email": "muhaiminrahmat@gmail.com",
    "phone": "085348109499"
}'
```
Get All Students
![Get All Students](img/list.png "Get All Students")
```shell
curl --location --request GET 'localhost:8080/api/students'
```
Update Student
![Update Student](img/update.png "Update Student")
```shell
curl --location --request PUT 'localhost:8080/api/students/1' \
--header 'Content-Type: application/json' \
--data-raw '{
    "firstName": "Uzumakssi",
    "lastName": "Naruto Hokagess",
    "email": "adsadas@konohagakure.co.jp",
    "phoneNumber": "9779797979"
}'
```
Find Student by ID
![Find Student by ID](img/find.png "Find Student by ID")
```shell
curl --location --request GET 'localhost:8080/api/students/1'
```

Delete Student

![Delete Student](img/delete.png "Delete Student")

```shell
curl --location --request DELETE 'localhost:8080/api/students/4'
```