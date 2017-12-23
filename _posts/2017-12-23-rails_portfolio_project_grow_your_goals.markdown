---
layout: post
title:      "Rails Portfolio Project: Grow Your Goals"
date:       2017-12-23 10:48:40 -0500
permalink:  rails_portfolio_project_grow_your_goals
---

![](http://78.media.tumblr.com/1325948d2400b59fc5261f9dc67028ac/tumblr_ovf6t6qWnZ1tugqfdo1_540.gif)

Another day another drama, drama…Or at least another infuriating bug on the way to my Rails project! 

That was the theme of the start of this project. It took me a little while to get my sea legs. Which is true of this project, but also Rails in general. 

It was slow going through this project, but I’ve finally made it! My app is done and I couldn’t be happier. 

For this project, I created a goal tracking app that lets users create a goal and fill it with the tasks or actions they need to take in order to achieve that goal. This turns out to be a very important distinction of words. I personally prefer “actions”, because the app is meant to track high level goals and “tasks” just seems like your run of the mill daily to-do list (But more on that later!)

The general idea was to help users track big life goals, but also help them think about what actionable steps they could take to finally achieve those goals. This kind of tracking and brainstorming can help take you from “I’ve always wanted to write a novel” to “My unpublished manuscript is sitting in a desk drawer!” ( *I kid* ). Instead of the traditional daily to-do list, you think of actions you can take to bring you one step closer to your big life goal. My app helps users do just that, by visualizing their goals as plants, and with each completed action (or task as the word may be), their plant (goal) grows. Below you can see the lifecycle of a goal (in plant form)…thus, “Grow Your Goals”. 

![](https://i.imgur.com/dCVGNsN.jpg)

I created the graphics for each stage of the plant’s lifecycle (it looks way less blurry than this image IRL), as well as a logo for the header of the website. 

I like to layout a wireframe of sorts before I start a project like this, visualizing the UX helps me a lot with planning the app, even in the beginning. Being able to see the page helps me realize what I want on it, which leads me to thinking about what I need to build to make that happen. 

With this project I tried using a new tool, Adobe XD, and let me just tell you…I LOVE IT. It’s awesome and super easy to use. You can link parts of the page together to show how the app flows and how a user might interact with it, and you can also publish it online to get easy feedback. 

Truth be told, it took me awhile to find the right project for this assignment. I had quite a few ideas, but it took some time to figure out how to fit each idea to match the requirements and plenty of them just didn’t make sense or work. But eventually I settled on this one and work began! Yay. 


The biggest problem I encountered while building this project was my choice of model name. Insert dramatic, depressed sigh here. (Remember how I said “more on that later”? Welcome to later…)

Originally I had chosen to go with “Goal” and “Action”. Which was all well and good…for awhile. Everything was just dandy until I started building the controller actions for “Action” (should that have been my first clue?) and I had to build my action_params method so I could whitelist my params, because as we all know, we don’t trust things from the big scary internet! 

So I was being a good little coding student, I wrote my nice params method and went on my merry way. 

*What big eyes you have, Grandma. The better to see you with, my dear.*


After literal hours of frustration, sweat, and tears (or you know, something considerably less dramatic.) I came to the stunning conclusion (read: guess) that I should check to make sure “Action” wasn’t a reserved keyword. 

I mean, it worked LITERALLY everywhere else in the project and nary an error or warning in sight. So why would it have so much trouble with:

```
def action_params
    params.require(:action).permit(:name, :goal_id)
end
```


*What big teeth you have, Grandma. The better to eat you with, my dear!*


Sure enough, there it was…the word “action” under unlisted reserved keywords in Rails. *slams head onto desk repeatedly*

And when I changed the model name from “action” to “task”…voila! It’s works. No more angry errors. 

**TL;DR Always check to make sure your model names aren’t reserved keyword. **

That was by and large, the worst of the troubles I encountered during the course of the project, and after I got it figured it out it was smooth sailing until the end. 

Once I got everything working, I used Sass to style it and make it look relatively like the mock up I created with Adobe XD.  I even included working progress bars and a growing plant image! I’m looking forward to streamlining and further improving this project in the next section. 

Until then, keep Dumblin’!

![](https://i.imgur.com/qhnJO.gif)


Yep. I’m reusing this gif because it’s amazing.





