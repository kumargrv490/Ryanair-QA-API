Task overview 
Feature: User management
  As an API client
  I want to manage users
  So that I can create and retrieve user data

  Scenario: Create a new user successfully
    Given I have valid user data
    When I send a POST request to "/user"
    Then I should receive a 201 response
    And the response should contain the created user's details

  Scenario: Retrieve a user by ID
    Given a user exists with ID 1
    When I send a GET request to "/user/1"
    Then I should receive a 200 response
    And the response should contain user details
Doumentation to Test steps-
Setup instructions (Docker + test install)
 **Run the API service**

   ```bash
   docker load -i api_testing_service_latest.tar.xz
   docker run -d -p 8900:8900 --name apiservice api_testing_service
Run instructions
*Install dependencies/
*Create Java projet<RestAssuredApi
*Write Automation API Tests Scripts 
Framework choice rationale
I have used TestNG becouse I am familiar with with this framework.
Test coverage explanation (which endpoints, what’s validated)-
* User resource
Create user (201)
http://127.0.0.1:8900/user
Get user by ID (200)
http://127.0.0.1:8900/user/1
*Booking resource
Create booking for user (201)
http://127.0.0.1:8900/booking
Get booking by ID (200)

http://127.0.0.1:8900/booking/1

Report access instructions-
file:///C:/Users/kumae/eclipse-workspace/RestAssuredAPI/test-output/index.html
