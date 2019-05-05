# testpythonbackend

API tests for python based web application backend. Tests are written using postman, based on the supported API's as descibed in swagger documents.
Run the tests:
Import Potsman collection to POSTMAN gui to run it. On CI/CD system there are few ways tests can be run.

Option 1: Use docker to run postman collection:" docker run -t postman/newman:ubuntu  run https://www.getpostman.com/collections/5ebb5740cd3d4d8182fe"
To copy collection URL please copy the link from postman UI. These tests will send API calls to localhost:5000, make sure the server is running on this port or change the URL if its runnig elsewhere. For real production system API will be deployed to Cluster and postman collection will be on the same or different cluster.

Postman is used with newman to run these tests.
