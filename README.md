# springboot-dynamodb
## Simple Spring boot project to connect with Aws Dynamo DB with basic crud operations.

```diff
- In application.yml file change the Dynamodb related credentials.
```
## Create a user with Administrative privileges.
```yaml
-access:
    key: 
    -secret-key: 
  region: ap-south-1//The region where u created the DynamoDB.
  end-point:
    url: dynamodb.ap-south-1.amazonaws.com
    server:
  port: 9001
```  
 
## Sample rest end points.
```
 http://localhost:9001/dynamoDb
 Method—PUT
 Request Body
json
 - {
    "studentId": "a548916e-79a3-4dd2-85c3-4534e2a79d32",//Primary key for updating the record
    "firstName": "Jonathon",
    "lastName": "Request",
    "age": "19"
 }

- http://localhost:9001/dynamoDb
Method—POST
Request Body
{
    "firstName": "Stephen",
    "lastName": "raids",
    "age": "19"
}
http://localhost:9001/dynamoDb?studentId=7718c0b5-594f-4663-854e-89506625c8d7&lastName=raids
Method—GET
Sample Response
{
    "studentId": "7718c0b5-594f-4663-854e-89506625c8d7",
    "firstName": "Stephen",
    "lastName": "raids",
    "age": "19"
}

