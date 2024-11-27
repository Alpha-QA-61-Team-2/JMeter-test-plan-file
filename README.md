# WEare Social Network Performance Testing
This repository contains JMeter test plan for performance testing of the WEare Social Network App.

# Prerequisites
1. Apache JMeter: Download and install Apache JMeter.
2. WEare App: Ensure the app is running locally or on a server.
3. Test Data: Make sure test data (e.g., test user credentials) is available.

# Test Scenarios
The following actions are simulated to test the app’s performance:

- Register User: Simulate user registration by sending POST /register.
- Login: Simulate users logging in with valid credentials via POST /authenticate.
- Get Posts: Simulate users fetching a list of posts using GET /posts.
- Create Post: Simulate users creating a new post via POST /posts/auth/newPost.
- Update Post: Simulate users updating an existing post via POST /posts/auth/editor/{postId}.
- Delete Post: Simulate users deleting a post via GET /posts/auth/manager/{postId}.

# Running the Tests
1. Import Test Plan: Open JMeter, go to File > Open, and select the weare_social_network_test_plan.jmx.
2. Configure Test: Modify Thread Group settings (number of users, ramp-up, loops).
3. Run Test: Click the Start button in JMeter.

# Analyzing Results
Use Summary Report and Aggregate Report to view key metrics such as response times, throughput, and error rates.
View Results Tree is useful for debugging failed requests.

# Notes
Run tests in a staging/test environment to avoid impacting production.
Monitor server resources (CPU, memory) during tests.
Adjust the number of threads and ramp-up time based on your testing needs.
