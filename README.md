Integrating Server Side Authentication/Authorization
In this lab, you will be integrating all the lectures and walkthroughs of Server Side Concepts to one of your full stack labs. Blogs or Chirper, or both for the additional practice! The goal of this lab is to be able to run the tests successfully in Postman that the series has discussed.

 

NOTE DO NOT PUSH YOUR JWT SECRET KEY TO GITHUB. Make sure their values are in the .env and that is added to your .gitignore as well. If you're worried, paste some screenshots of .env, config/index.ts and .gitignore to Discord and we can confirm it looks correct.

 

Instructions
Install the required node modules as referenced in the Lectures and Walkthroughs

Add the appropriate API Endpoints to your Express server for handling a login and register request

e.g. POST /auth/login and POST /auth/register
Choose the appropriate endpoints to protect behind the JWT Strategy with passport

e.g. most POST, PUT, and DELETE requests should be private. GET may vary, just ask yourself, "should this request require someone to be logged in first?"
Make sure the following tests work in Postman

POST /auth/register adds a new user to your database and sends a token as a response
POST /auth/login validates a user's credentials and sends a token as a response
any protected endpoint should 401 status code you if no token is provided, and work normally if a token is provided
if adding this to your Blog or Chirper labs, use the req.user.userid in your POST requests as the authors/writers
e.g. if req.user.userid of 1 is logged in, then that is who should be inserted into the database for that row