---
layout: post
title:      "A CLI to Search for Trails in Florida"
date:       2019-10-29 00:32:11 +0000
permalink:  a_cli_to_search_for_trails_in_florida
---


For my first project I created a CLI application to find mountain biking trails in Florida, and narrow results by location or difficulty. My process closely followed the example give by Avi in his video walkthrough of creating a CLI gem. I chose my website to scrape information from (https://www.mtbproject.com/), layed out a basic plan for the interface of the application, and then began writing code adding functionality as I went along.

As Avi did, I began coding the logic for my CLI. Eager to move on to the my Scraper and Trail classes, my initial CLI was messy, and the logic convoluted. Later in the project, I had to clean up my original code, and this proved to be a tedious task. I should have written cleaner code for my CLI in the first place, or refactored my messier code before moving on to other classes. 

The Scraper class method trails returns an array of hashes, each hash holding the data to create one trail instance. The Trail class method scrape_trails iterates through the array returned by Scraper.trails, and creates a new Trail instance from each hash. This all occurs as soon as the the CLI is started. 

The user can then choose to look at all the trails in the state, or narrow results by location or difficulty. After the list is narrowed, the user chooses a trail to look at, and all the information for that trail is printed to the terminal. 

The biggest obstacle I faced while writing this program was refactoring my CLI logic. The tedious nature of the work made it an annoying task to complete at the end of the project. You can find the github repo for my application here: https://github.com/zacharytq/sfl_mtn_bike
