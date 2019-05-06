# Test python backend

Tests written using postman, based on the  API's contracts as descibed in swagger documents.
Run the tests:
Runnng tests with postman GUI:
Improt the collection from repo into Postman and execute the collection run, results will be displayed on the GUI.

Running tests with docker:

Make sure you have docker installed
docker run hello-world
Pull the docker image with postamn and newman instaleld already:
docker pull postman/newman:ubuntu

 On CI/CD system there are few ways tests can be run.

Option 1: Use docker to run postman collection:" docker run -t postman/newman:ubuntu  run https://www.getpostman.com/collections/22538fb42f3e286b552f"

To copy collection URL please copy the link from postman UI:
Click on the collection on Postman GUI, click "share collection" and get link to copy the URL to clipboard.
These tests will send API calls to localhost:5000, make sure the server is running on this port or change the URL if its runnig elsewhere. 
For CI/CD system API will be deployed to Cluster and postman collection will be on the same or different cluster.

Test results analysis:

There are serious bugs with just minimum set of tests, also app does not seem to recover from failure i.e. if there are test run failed during first test run, follow on tests most of the tests will fail. There are more possible combinition of tests which should make part of suite of tests for API as well as exploratory testing to find more issues related to load and performance testing of the API.
