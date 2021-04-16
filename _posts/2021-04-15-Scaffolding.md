you can use rails g scaffold book title:string description:text and you can use ruby on it's own to build a "scaffold" for you to work within.  

You just have to use rails g for generate, give the controller/views name and then give the database tables titles and data type (strings, integers, etc)
for it to create based on.

if a view template is within another view template you have to name it with a _ in front of it like _books.html.erb before it will render for you
you can then render that on top of other views

"Before action" and "after action" will happen before a paritcular action happens.  Thes are in your controllers
Before actions are primarily used for login/authentications as a security measure

in the controller there are a number of defined actions
those defined actions will say things like "render XYZ.html.erb" and it will look at that view and render whatever is happening there
