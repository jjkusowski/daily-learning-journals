# Learning Journal Code 301 Project Week Monday

## Team Members
- Phelan Carey
- Matt Iwicki
- Ariel Pedraza
- Jeff Kusowski

## Project identification
We decided over the weekend to do a Marvel Comics themed app using their well-documented API.  Monday morning, we had to sketch out what it would exactly do and what the architecture would look like.  We decided to make it based on the Events in the Marvel universe (e.g. Civil War, Infinity Gauntlet) and display to users the characters and comics that were involved in those events.  Stretch goals are to let users filter Events by the characters that are in them.

## Architecture
Some of this is still fluid as we learn more about the API, but initially we will be only using local storage to cache all the information we pull from the API.  We may choose to populate an SQL database if we find ourselves making too many API calls or if the API proves to be too slow.  

## Getting to the Haxxing
We started off with Matt and I paired together working on backend while Ariel and Phelan worked on front end.  Matt and I got the API call to Marvel working and returning Event results to the browser.  We also made the client-side JS to accept the data and pass it through a constructor.  The hardest parts were figuring out the md5 hash that the API required for us to pass in (none of us had ever heard of that, though it proved straight-forward) and sorting through the payload that returned to get only the information that we wanted.  For example, the comics and characters associated with each event were several levels down in the object along with creators (writers, inkers, etc) and other information that we didn't want.

## Day 1 results
At the end of the day, we had 20 events being returned each with 20 characters and 20 comics for each.  The events and their images are displayed on our page.
