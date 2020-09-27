---
layout: post
title:      "Just Around the Corner"
date:       2020-09-27 19:39:26 +0000
permalink:  just_around_the_corner
---


I have always struggled with shopping for gifts. Whether it be for birthdays or the holidays, I put off shopping until the very last minute and end up buying a gift that I don't think is very thoughtful or not buying a gift at all. In an attempt to be a better friend, I have started keeping track of gift ideas for my friends and family through out the year. Whenever a friend mentions a thing they desire or an idea strikes me for a gift, I immediately record the idea to a spreadsheet. Now whenever I have to buy a gift, I have a list ready to go for all of my friends. Just Around the Corner implements this idea into a webapp.

I built the app using the MVC (Model View Controller) paradigm. The app has three models: User, Friend, and Gift. Gifts belong to friends and friends belong to users. After logging in, the app takes you to a page that lists all of your friends that you're tracking gifts for, and lets you know how many more gifts you have left to get for them. You can add a new friend in a form that comes after all the cards with friends on them. 

Navigating to the individual friend page shows you a list of all the gifts on your list, and gives the options to mark as purchased or delete from the list. On this page, after all the cards with gifts on them is a card with a link to a page to make a new gift. All form fields must be filled out to make a new gift and failure to fill every field out will result in the user being redirected to the gift create page again.

I used bootstrap to quickly create a card based design logic for the friends and gifts. Bootstrap also privided the framework to make the navbar. With bootstrap it was easy to have my content automatically adjust the size and shape of the the containers i had my content in. For tablet and phone sized view-ports the navbar automatically includes a hamburger menu, and the cards that hold content form a single column on phones instead of a row across the screen. There are some design features I'd like to refactor eventually. For example, the friend cards don't begin to wrap at a breakpoint that makes sense for many tablets. 

Just Around the Corner taught me more about integrating design elements than anything else. With all of the practice making MVC apps over the course of the Sinatra module, the apps scaffolding came together very quickly. Integrating bootstrap and attempting to make my app look better while maintaing the same functionality proved to be a more difficult task. But I think the end result is a respectable, albeit simple, app that could actually help me be a better friend.


