## Week Three Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What are the 3 main features in an ERD?
  * Noun (restaurant), the path (many or one), and the verb ("has").
2. Create an ERD for the following database: Restaurants, Customers, Items, Ingredients, Beverages, Orders, Vendors.
  * See drawing
3. What is the entry at the command line to create a new rails app?
  * `rails new my_app_name`
4. What do Models generally inherit from in rails?
  * `ActiveRecord::Base`
5. What do Controllers generally inherit from in a rails project?
  * `ApplicationController`
6. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  * `resources :horses, only: [:show]`
7. What rake task is useful when looking at routes, and what information does it give you?
  * `rake routes`
  * I see a table of all the routes showing prefix, verb, URI pattern, controller#action
8. What is an example of a route helper? When would you use them?
  * A route helper is the prefix with `_path` at the end.  I would use a route helper when writing links.
  * Ex: `link_to @horse.title, horse_path(@horse)`
9. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  * `_url` returns the complete url, whereas `_path` returns just the relative path (everything following the root).
10. What are strong params and why are the necessary?
  * Strong params validate that ONLY the params requested are compiled into the database.  They are an extra security measure to ensure someone doesn't force a "sudo param" into your application.
11. What role does `form_for` play in helping us create our forms?
  * `form_for` is a rails method that generates the HTML necessary for creating forms.
12. How does `form_for` know where to submit the user's input?
  * The variable passed in on the first line determines the destination. Ex `form_for(@horse) do |f|`
13. Create a form using a `form_for` helper to create a new `Horse`. 
  *
```ruby
form_for(@horse) do |f|
  f.label :name
  f.text_area :name
  
  f.submit
end
```
14. Why do we want to validate our models?
  * To ensure that inputs are unique, present, etc.  It generates errors and eases database management.
