Code Challenge Interview

If anything seems to not be working, feel free to reach out to me, this interview kit is always in constant change, hopefully with very few broken builds!

Welcome! Your task is to create a website that displays some data from an API.

You can use whatever languages and frameworks you are comfortable in your stack so long as the code works. Our stack in the office is React+TypeScript on top of a Node.js+TypeScript (REST and GraphQL) backend.

If you manage to host your project online, it's a plus but definitely not a requirement.

To complete the interview:

1. To obtain your authentication token, Send a POST request containing your email (using "email" as the key, with the body formatted as raw JSON) to
   https://welbi.org/api/start

   From now on, the token is to be sent with all queries as an authorization header, with the shape (More information on the Bearer Authentification)
   Authorization: Bearer [the token goes here]

2. Build your front end to display all the programs and their attendees in whatever manner you deem appropriate
3. Commit your code to a Github repository
4. Send a POST request containing a link to the repository (using "url" as the key, with the body formatted as raw JSON) to
   https://welbi.org/api/finish

To use REST:

1. Fetch a list of residents by sending a GET request to
   https://welbi.org/api/residents
2. Fetch a list of programs by sending a GET request to
   https://welbi.org/api/programs
3. Send a POST request to the same routes to create a new resident and a new program, body needs to be raw JSON
4. Attend the new resident to the new program by sending a POST request to
   https://welbi.org/api/programs/[programId]/attend

To use GraphQL:

1. Fetch a list of residents and programs by sending a request to
   https://welbi.org/api/graphql
2. Create a new resident and a new program by sending a request to the same route
3. Attend a new resident to the new program by creating a new attendance record
