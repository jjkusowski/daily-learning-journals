# Learning Journal Code 301 Project Week Tuesday

## Morning
This morning we divided up into the same teams as yesterday, but switched roles between front and back end.  So Matt and I worked on the "Event" page in the html, focused first on a mobile view.  We got that working around lunchtime.

## Afternoon
Matt and I continued to work on the index page, but moved on to desktop view.  We put in several @media breakpoints so that the site displays 4, 5, or 6 images at a time, depending on how wide the browser is.  I also made a logo for the page.

## Data storage
A running theme for the day was deciding on and implementing our architechture for holding and retrieving our data.  There are over 1400 characters and 40,000 comics that we want to be able to retrieve and have image URL's for.  Doing that through the Marvel API is not viable since we are limited to 3000 requests per day per API key.  Those would be used up quickly by a user since a single page view could have over 100 characters and comics to display.  So we eventually decided to download all the data in development and store them in an object on the server.  The file size appears that it will be too big to store in localStorage.  So we have to leave it on the server.  Now we have to decide if we can pull the data we need for a particular page view server-side and send it to the browser or if we just send the whole file over at page load.
