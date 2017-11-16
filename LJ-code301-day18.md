# Learning Journal Code 301 Project Week Wednesday

## Morning
In the morning, we rethought our our plan to use a JSON file to store our data.  That led us to relook at the available API's to see if we could use them directly in a better, smarter way.  We found API's that we had previously overlooked that returned the data that we needed without sending dozens of calls that would both slow us down and cause users to max out our daily allowance of API calls to Marvel.

We got to work on refactoring our code to make the necessary calls.  By lunch, we had the calls correctly returning data, but not quite handling it correctly on the client side.

## Afternoon
After lunch, we got the constructors putting the data into arrays properly, but encountered big async issues.  Our function to display the data was being called prior to the API's returning our data, so on the first request, our page wouldn't display any data, and on subsequent requests, it would display the data from the previous request.

We then went down two parallel paths.  The first was relatively simple in that we forced the page initialization method to be called twice, once at the end of each API call.  This causes the page to write twice, but it's not incredibly noticable to the user.  However, it's not ideal.  We also worked on seeing if we could completely separate the two API calls and write their subsequent data separately, rather than writing all the data to the page twice.
