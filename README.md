# SaaS-MVP-Engineering

Welcome in this online course on SaaS MVP Engineering.


# Assignment 3
You have the skeleton of the MVP up and running. Let's start to add what we think is the minimal feature set of for our application. Mind that this is just a simple MVP for the purpose of this bootcamp, I'm pretty sure you won't impress a large number of users with this ;)

Here is what we will be doing in this assignment:
1. Introduce a new page with a "Connect to Twitter" button.
1. Implement connecting to Twitter once the user presses this "Connect to Twitter" button.
1. Change the routing so that a user that is not yet connected to twitter is automagically redirected to the connect-to-twitter page
1. Introduce a page where a logged in user can enter up to 3 keywords she wants to track on Twitter
1. After submitting these keywords, save these keywords, start a twitter stream on these keywords, save incoming tweets into the database and show the user a real-time timeline of tweets matching her keywords.

For each of these steps, there are detailed walkthroughs in the Git Repo

### 3.1 Adding a "Connect to Twitter" button.

#### Introduce a new authenticated route /connect-to-twitter
Go to routes-authenticated.js and introduce a new route /connect-to-twitter as follows:
````javascript
Router.route('connect-to-twitter', {
  path: '/connect-to-twitter',
  template: 'connectToTwitter'
});

````
Be sure to hit http://localhost:3000/connect-to-twitter to test if that route works!


#### Introduce a new page with just a button on it, saying "Connect to Twitter"
In client/views/authenticated/ introduce a file called connect-to-twitter.html. This file will contain the html for the button.
In client/controllers/authenticated/ introduce a file called connect-to-twitter.js. This file will contain all the logic and event handling and so one.

In connect-to-twitter.html, add the html for the button
````html
<template name="connectToTwitter">
  <a id="connect-to-twitter" class="btn btn-success">Connect to Twitter</a>
</template>
````

In connect-to-twitter.js, add an onClick event handler to our button.
````javascript

Template.connectToTwitter.events({
  "click #connect-to-twitter": function(event, template) {
    alert("clicked");
  }
});
````
