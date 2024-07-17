Description
Implement REST APIs to streamline and automate the process of managing shipments for 
businesses involved in shipping goods. The API should enable users to retrieve a particular 
shipment information based on the specific trackNo and also delete the requested shipment 
data based on the requested shipId.
Entity Details
The Shipment entity should have the following attributes:
● shipId : the id of the Shipment (Integer) (unique)
● trackNo : the track number of the Shipment (String)
● origin : the origin of the Shipment (String)
● destination : the destination of the Shipment (String)
● status : the status of the Shipment (String)
Here is an example of a Shipment JSON object:
{
 "shipId": 1,
 "trackNo": "TRK001",
 "origin": "New York",
 "destination": "Los Angeles",
 "status": "In Transit"
}
You are provided with the implementation of the models required for all the APIs. Your task is to 
implement a set of REST services that exposes the endpoints, retrieves a particular shipment 
information based on the specific trackNo and delete the requested shipment data based on 
the requested shipId:
| API Route | API Type | Success Response Code | Validation Error Code |
|-------------------------|----------|------------------------|------------------------|
| /shipment/{trackNo} | GET | 200 | 404 |
| /shipment/{shipId} | DELETE | 200 | 404 |
Task 1:
GET request to /shipment/{trackNo}
Retrieve shipment details by trackNo.
Response Body: JSON object representing the shipment details.
HTTP Status Code:
● 200 (OK) - If Shipment with the specified trackNo found and returned.
● 404 (Not Found) - If Shipment with the specified trackNo not found.
Task 2:
DELETE request to /shipment/{shipId}
Delete shipment details by shipId.
Response Body: String object should give the response as "The requested shipId-3 got 
deleted" for correct shipId and response
HTTP Status Code:
● 200 (OK) - Shipment Id, i.e., the shipId found and deleted.
● 404 (Not Found) - Shipment with the specified shipId not found.
Task 3:
ShipmentService
● Implement the GET method which should return a Shipment data based on trackNo.
● Implement the DELETE method which should delete a Shipment data based on shipId.
Complete the given project so that it passes all the test cases when running the provided unit 
tests.
Files in which you need to write the code:
● src/main/java/com/example/shipment_model/controller/ShipmentController.java
● src/main/java/com/example/shipment_model/service/ShipmentService.java
Example Requests and Responses:
GET request to /shipment/{trackNo}:
The response code is 200 and the response body, when converted to JSON, is as follows:
Request: GET - /shipment/TRK002
 {
 "shipId": 2,
 "trackNo": "TRK002",
 "origin": "London",
 "destination": "Paris",
 "status": "Pending"
 }
DELETE request to /shipment/{shipId}
The response code is 200 and the response body should return a message as follows:
Request: DELETE - /shipment/3
The requested shipId-3 got deleted
You can use the MySQL shell to view the data and query the tables
