# RESTful-API-with-Swagger
Here an API for building sensor network is designed with Swagger 2.0. 
API Requirements:
Models: Two models are defined in the API's definitions: Building and Sensor.

1) Building:

Properties of Building objects:

• id: unique string

• name: string

• address: an object with two properties:

    ⁎ Street address: string
    
    ⁎ Post Number: integer
    
2) Sensor:

Properties of Sensor objects:

• id: unique string

• name: string

• value: number

• state: enum (posssible values: "online", "offline", "error")

It is assumed that there is a database that has linked the Sensors with their corresponding Buildings and that all of these IDs are known. Therefore, Building ID under the sensor separately are not added here, or create methods into the API to retrieve these IDs from the database. 

Methods:
The attributes, HTTP methods and functionality required from the API are defined here. 

• GET method to receive all Buildings.

• GET method to fetch a Building with a specific Building ID.

• POST method for adding a new Building. Building data is included as JSON in the message body.

• PATCH method for updating a Building with a specific Building ID.

• PUT method for adding a new Sensor.

• DELETE method for removing a Sensor.

• GET method to retrieve all sensors in a Building that has a specific Building ID.

• GET method to retrieve all sensors in certain state(s). State(s) MUST be specified as querystring.
