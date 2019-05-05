# testpythonbackend

Tests for python based web application backend. Tests are written using postman, based on the  API's capabilities as descibed in swagger documents.
Run the tests:
Import Potsman collection to POSTMAN gui to run it. On CI/CD system there are few ways tests can be run.

Option 1: Use docker to run postman collection:" docker run -t postman/newman:ubuntu  run https://www.getpostman.com/collections/22538fb42f3e286b552f"

To copy collection URL please copy the link from postman UI:
Click on the collection on Postman GUI, click "share collection" and get link to copy the URL to clipboard.
These tests will send API calls to localhost:5000, make sure the server is running on this port or change the URL if its runnig elsewhere. 
For CI/CD system API will be deployed to Cluster and postman collection will be on the same or different cluster.

To run tests you need to install postman as well as newman (a command line run tool).
There are quite a few bugs with just minimum set of tests, also app does not seem to recover from failure i.e. if there are test run failed during first test run, follow on tests most of the tests will fail. There are more possible combinition of tests which should make part of suite of tests for API as well as exploratory testing to find more issues related to load and performance testing of the API.
