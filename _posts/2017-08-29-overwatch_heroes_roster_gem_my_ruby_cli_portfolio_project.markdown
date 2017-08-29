---
layout: post
title:  "Overwatch Heroes Roster Gem: My Ruby CLI Portfolio Project"
date:   2017-08-28 21:26:27 -0400
---


My first portfolio project: the night was dark and full of terrors, but (phew!) I finally made it through to the end.  The goal of this project was to create a CLI application that scraped data from a website and presented it to the user (at least two levels deep, i.e. a list of some kind and then further information about each list item). 

I brainstormed a few ideas, but eventually I settled on the one that turned into my project. A roster that displays all of the current heroes available in the video game Overwatch. Overwatch is a team based shooter that features (currently) 25 unique heroes with their own abilities and histories. In my gem, a user can see a list of all the current heroes and then see more information about each individual hero (by typing their name in the console). 

The information that is available for each hero includes biographical information (such as: real name, age, and location) a list of their abilities and what they do, a brief overview description of the hero, and a quote. 

In order to build this gem, I scraped the main page that lists all of the heroes in Overwatch (https://playoverwatch.com/en-us/heroes/), to generate the roster for the user to view. Then, when the user selects a hero, my gem uses information from the first scraping (a partial URL) to create the full URL of the hero’s individual page on the Overwatch site and scrape the necessary information from that page. It then fills in the rest of the information in the appropriate Hero object which was created as a shell at the beginning of the program. 

It was necessary to create each Hero as a shell with only a name and partial URL, because when I created them complete (with all of their attributes) at the beginning of the program it caused significant slow down to the program. There was a long and very noticeable delay before the list of heroes generated in the console. This way, the heavy lifting is only done once the user actually requests more details about a Hero and unnecessary scraping isn’t being done. 

To prepare before coding the gem, I read the instructions, watched the walkthrough video, and broke everything down on a Trello board to help me plan and organize my thoughts as I figured out how to implement what I needed to do. I really think having the Trello board helped a lot during the process of the project, as oftentimes I find that the hardest part isn’t the actual coding but sorting out the logic behind what you are trying to accomplish before you even start. 

Once I started building, unsurprisingly, I encountered a few struggles. One such example is a problem I encountered when processing user input. In my gem, the user selects the hero they want to see more details about by typing the hero’s name into the program, the problem occurred with two of the heroes who have special characters in their name that are not present on a standard English keyboard (Lúcio and Torbjörn). If you tried typing in the name without the special characters the program had no clue what you wanted. There were a few options to solve this problem, and in the end I added logic to substitute the special characters for their equivalent character on the standard English keyboard. Now the user can type in the simplified version of the characters name and see the correct results.

I used some helpful tools, bundler and colorize, in the creation of my gem. As Avi suggested in the walkthrough video I did some research on using bundler to create gems and watched the Railscast video in order to learn how to use it effectively. There is a lot to dig into with bundler and it can be easy to fall down the rabbit hole and spend so much time researching that you delay actually getting started. 

That definitely happened to me, but luckily I was able to course correct and the work I put in before getting started helped me to get back on track. Having a solid understanding of what you want to do with your program and how you want to achieve it makes a big difference.

As for Colorize, it was just a fun little addition I wanted to include, to make the large amount of text in the gem easier for the user to consume and to add some visual separation to the information presented. 

All in all, I am thrilled to be done with my first portfolio project. Sometimes when I’m starting with a blank canvas on a project like this, it can seem daunting and almost impossible, but that just makes it all the more satisfying when it all finally comes together. Puzzling over a problem is one of the best parts of coding, but seeing your efforts come to life in a working program just can’t be beat. Until next time, fellow coders! 


