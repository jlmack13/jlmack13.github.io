---
layout: post
title:      "Rails/jQuery Project Blog Post"
date:       2018-02-25 16:08:33 +0000
permalink:  rails_jquery_project_blog_post
---



In this project, we were required to revisit our Rails project and add new features using jQuery and Active Model Serializer (AMS).  Some of the new features we were required to build include:

## The Index Page
* Render an Index page via jQuery and AMS. For example, in my project, after the user logs in they now see a “Show Goals” button. When the user clicks this button the index of their goals is rendered using jQuery and the API I created using AMS. 

## The Show Page
* Render a Show page via jQuery and AMS. For this requirement I added “Next” and “Previous” buttons to my Goal Show pages that, when clicked, (…you guessed it!) render the next or previous goal without refreshing the page. Adding this functionality to my show page also allowed me to satisfy the next two requirements as well. 
* The rails API must reveal at least one has-many relationship in the JSON that is then rendered to the page. Since my goals were being rendered to the page via JSON already, it was a simple matter to include their tasks and render them as well. 
* Must use your Rails API and a form to create a resource and render the response without a page refresh. For this requirement, adding a new task to the goal show page made the most logical sense. Now, when a user wants to add a new task on the show page, they simply fill out the form and hit submit. Voila! The new task is appended to their task list without the page being refreshed. 

## The Final Requirement 
* Must translate the JSON responses into Javascript Model Objects. The Model Objects must have at least one method on the prototype. This requirement was met naturally throughout the course of building the rest of the new features. I translated both Task and Goal into Javascript Model Objects and for each I created a prototype method that formats the HTML to be appended to the DOM when they are rendered. 

And that’s that! Time to move on up  to React and the final project.


####  Bonus: 

Something I learned during this project...

To escape `git diff` you have to type `q` instead of `exit` or `ctrl—c`



![](https://media.giphy.com/media/lzZQRZN3MBXbO/giphy.gif)
