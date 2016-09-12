## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
  * A way to store data on the local machine and allow that data to be accessed across any of the app's webpages.
* What’s the difference between a session and a cookie?
  * A session encrypts the data, a cookie does not encrypt the data.
* What’s a flash and when do you want to use flashes?
  * A flash is similar to a cookie and session, except the data is only stored in a flash for one instance.
* Why do people say “HTTP is stateless”?
  * Because HTTP does not maintain state...  That is to say, variables and other data points are not accessible anywhere after the HTTP response is sent.
* What’s authentication? Explain.
  * Authentication is what allows a user to log in and verifies their information is correct... and they are who they identify to be.
* What’s the difference between authentication and authorization?
  * Authorization, on the other hand, is what verifies a specified user is able to access a given area in the app.
* What’s a before filter?
  * A before filter executes a given action before whatever is declared.
* How do we keep track of a user once they’ve logged in?
  * There are several ways to keep track... one of the main ways is to store their id (or some other identifier) in sessions.
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  * Namespacing a resource allows you to dictate where certain users can access.  A perfect example is namespacing an admin.
  * Nesting resources is usually used with a user OWNS a lot of whatever.  Keeps user paths separate.
* At a high level, what tools can you use to implement authorization? How would you use them?
  * Namespacing, helper methods and before actions.  Make sure a user is an admin before ANY action in the namespaced admin controllers.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  * An enum is a way to change an integer to an accessible string.  Simply put, the number correlates to an array of strings.
  * Declare the enum in the model.
* What are some strategies you can use to keep your views DRY?
  * Partials and helper methods.
