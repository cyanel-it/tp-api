# tp-api

# Architecture overview

Goal is to create a Hub API to access to objects across several museums API. It's a backend application that expose an API and make the usage of other API easier. First musuem is the Metropolitan of Art Museum API.

The global architecture is:

![High level architecture](docs/api-hub.drawio.png)

A request from a client application should be:

> Client application -- HTTP REQUESTS --> YOUR NEW API --- HTTP REQUESTS ---> One of the targeted museum

# Goal overview

Goals are:

* Design "YOUR NEW API" available at http://museumhub.com/api/v1/. This API has endpoints to search in different museums 
* Generates code of the API (for Python flask)
* Create a python application and integrate the generated API in a Python application
* Make your application up and running locally
* Add Mocks (samples) to test only the API
* Modify the application to call museum API instead of mocks

# Materials

- The Swagger editor at https://editor.swagger.io
- The metropolitan of Art Museum API documentation:  https://metmuseum.github.io
- Python on your computer
 
# Step 1: Think the API

To build the hub, we use one API first, the Metropolitan museum of Art. Remeber that this API has several endpoints we can use to create a search engine. At least two steps are mandatory:

- make a GET operation on "search" to get a list of objects ID (https://metmuseum.github.io/#search)
- make several GET operation on "objects/[objectID]" with each ID in search result (https://metmuseum.github.io/#object)

## Your Goal

Make a proposal for a new API which is able to make call across museums. Enpoints are:

- /search: look for object in museums with criteria and filters
- /museums: get info on museum, list existing museum
- /config: get server config like "number of items in pagination", the list of parameters

## Tips

- request must have a parameter to identify the museum (a code or unique id)
- request must have parameters to limit the number of result and browse into result pages (offest and limit)
- response should be the same, whatever your API result is
- response should contains error if something goes wrong
- When you define an API, You have to create objects to contains request and/or response data

# Step 2: Design the API with Swagger

- Go on https://editor-next.swagger.io
- Click on "Edit" menu and "Clear"
- Open another tab with the editor to have a sample code

## Tips

- You will define an "openapi" API
- The editor will help you to fill the file but not in all situation
- Also, you will have quick fix proposal and error message that you should follow
- Take time to analyze the sample code

If you are really spunky, you can use directly the specifications at: https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.1.0.md

# Step 3: Generate the code and analyse it

# Step 4: Create a Python application

# Step 5: Integrate the generated API

# Step 6: Run the application

# Step 7: Create mocks to simulate the Museum API

# Step 8: Test your application with POSTMAN

# Step 9: Change mock to call the museum
