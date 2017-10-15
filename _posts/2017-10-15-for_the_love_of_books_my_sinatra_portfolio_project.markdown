---
layout: post
title:      "For the Love of Books: My Sinatra Portfolio Project"
date:       2017-10-15 14:38:28 -0400
permalink:  for_the_love_of_books_my_sinatra_portfolio_project
---

## Guest Starring: Sass (and a lot of Harry Potter gifs)

Hello again. It’s time for another post about building a portfolio project!

## THE CHALLENGE

The challenge this time was to build an MVC app using Sinatra and ActiveRecord. The app had to have multiple models, at least one has_many relationship, and users (who could only edit their own content).  

## THE BACKSTORY
Earlier in this, my 29th year, I set myself the task of reading 100 books before my next birthday. One year. One hundred books. 

I’ve tried some version of this goal several times before, usually as part of a New Year’s resolution (we all know how well *those* turn out). 

![](http://www.reactiongifs.com/r/2013/07/Bitch-please-harry-potter.gif)

Alas, none of those attempts succeed

This time, however, I am *prepared*. This time, I’ve figured out how many books on average I need to read each week, each month, and I’ve got two separate methods of tracking which books I read and when. The thing is, they’re not great, they’re just okay. What I really need is an app to keep track for me…

![](https://userscontent2.emaze.com/images/3c722202-448b-4df4-8252-f9c62e0c0158/78350944-ae5b-446a-97b9-555d5277703e.gif)

Prior to this project, and heck even this bootcamp, I’d wanted to make a book tracking app that could fulfill all my bookworm dreams. A truly convenient, in-your-pocket, gorgeous, user-friendly, fully-featured app. This app is…not that app. But it’s a start in the right direction. 

This app is what I can do *now*, and since that is a heck of a lot more than I could do before I think that’s cause to celebrate! In the future, I hope to take this idea and keep building on it until it is that starry-eyed vision of an app I know it can be. But I digress, let’s get back to the present and I’ll tell you about what this app can do *right now*.

## THE APP

With this app you can create an account to track all the books you read, with the idea being that once you finish a book you add it to your list (and get one book closer to your goal, good job!). 

The app is private to the individual user, only you can see (and edit or delete) your books and your booklist.

You can add details to each book, if you wish, or you simply add the title and call it a day. The details you can track include: author, length of the book, what format you read the book in (paperback, etc.), and whether or not the book is one of your favorites. 

## THE BUILD PROCESS
As per usual, the first thing I did when starting this project was to think *a lot*. And then take a lot of notes. I found this [great article](http://blog.flatironschool.com/how-to-build-a-sinatra-web-app-in-10-steps/) by another Learn student (yay!) that helped me wrap my head around the structure I would need and the first steps I needed to take. It was a really good resource and I highly recommend it to anyone who needs a refresher or just wants to double check they’ve got all the right stuff set up on their project. 

Next, as I did with my last project, I created a Trello board to help me organize, plan, and keep the build process on track. This has been enormously helpful in getting my brain wrapped around a project. I usually start by writing out the requirements for the project and a checklist of the items I need to turn in. Then I create various boards for research, planning, building, etc. It really depends on the project and how organized my thinking is by the time I get to the Trello board. Most of it is useful, some of it never even makes it into the project, but its the best way I’ve found so far to plan my projects. 

Having my thoughts organized in advanced like this really helps keep the build process smooth.

To get started coding, I essentially went through the steps described in the article I mentioned above. Getting everything set up and ready to go. Once everything was in order, I created my migrations and models and tested them to make sure everything was in working order.

After that I started working on my Users. First I created the controller and filled out the first controller actions, I created a very bare bones view to test everything out and then I moved on to the next one. I continued this pattern of creating the action, building the view, and testing it out until I’d completed the user controller. In between, I did a little bit of styling as well. Although not necessary at this point, it helped me from a visual standpoint during the testing process. Once I was satisfied the with the users functionality, I repeated the same steps for books. 

## THE BUGS (!)
Of course the entire project didn’t go so smoothly, right from the start I encountered bugs and hiccups. During the beginning of the project, I was trying to test out my models, to make sure I had set them and my tables up correctly. Naturally, I run ‘tux’ in my console…only…wait a minute…I run into this:

`cannot infer baspath (LoadError) `

Well that’s new! I did some googling and started to get the impression that it had something to do with the require_relative statement I had in my config.ru file, but the answers online weren’t concrete enough for my satisfaction. At least until I found this: https://github.com/learn-co-curriculum/sinatra-complex-forms-associations/issues/29. Once again, another learn resource to the rescue! This mentioned that require_relative is not supported by Rack and changing it to a require statement ought to do the trick. Sure enough, I changed the require statement and I’m back in business with tux:

` require './config/environment'`

Hooray! Don’t you just love that feeling of detective work you get when you solve an issue? 


## THE GLORIOUS FINALE

After much building and testing (and building and testing), my app works and is ready for submission. But wait! Didn’t I mention Sass was going to guest star in this post? Time to talk about styling!

It wasn’t mentioned in the instructions that we should style our apps, but this time there was the opportunity to get some practice here and I wasn’t about to turn it up. I recently had the need to learn Sass (more on that in another post) and I was eager to brush up on my skills again. So instead of using plain old CSS to style this app, I did it entirely in Sass. 

Sass is great and if you haven’t tried it yet I highly recommend it. It’s like CSS but with a programmer’s logic applied to it. Why type a hex value 16 times (and have to change it in every location) when you can use a variable (and only change it once)?

To try and make my app both beautiful and functional,  I also used Bootstrap (and the Bootswatch theme Readable) and I created a logo for the header and icons for the details page.

If you want to learn more about Sass, check out [their documentation](http://sass-lang.com/guide). It’s really helpful and good for beginners. Or check out [Sass for Web Designers](https://abookapart.com/products/sass-for-web-designers) from A Book Apart. Perhaps you can’t tell, but I quite like reading. 

![](https://i.imgur.com/Tdcw9TW.gif)

And so, after putting the finishing touches on the styling and *much* testing I finished my project, and now I have a new tool to help me keep track of the books I’ve read! Until next time, fellow coders. 

![](http://cdn.smosh.com/sites/default/files/bloguploads/potter-gifs-dumbling.gif)


