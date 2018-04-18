---
layout: post
title:      "My CLI Data Gem Project"
date:       2018-04-18 01:32:24 +0000
permalink:  my_cli_data_gem_project
---


Hi My name is Judy.  This is my blog about the CLI Data Gem Project.

Over the Christmas holidays, I received a gift certificate toward the purchase of a meal kit from the website Chef’d.  After some initial research, I decided to do my CLI Data Gem project on meal kits.  I called my project “Chefilicious CLI Gem”.
I like the meal kit idea because: 
it is a good way of trying and learning about new cuisines;  
it provides a fun, convenient, and time saving way to prepare home cooked meals;  
and ingredients, measurements, and cooking instructions are included in a single package delivered directly to your home.  

Here is the thinking process I used for my CLI Gem Project: 
1) Planning
This was a critical step in my project because it provides a direction and a road map for my project.
I decided early on that my application would be a command line interface that allowed users to see the 50 top meal kits.  The user then would select their choice, see the information in detail, and click on the web-link that would take them directly to that website containing the selected meal kit.

 2. Next, I Installed a bundler gem to save time.
I used the command below to acquire a bundler gem:
 
            #bundle gem <chefilicious_cli_gem>
 
3.  I then created an Executable file, added it to the gem file, and placed it in the bin directory. The executable file should start with the code below:
 
            #!/usr/bin/env ruby
           
            It is important to remember to test the bin file to make sure your files are set up properly by using the following command:
 
            #./bin/chefilicious_cli_gem
 
You also might need to check if the permission is set up correctly by listing all the files (including the hidden files) in the current directory,  which is done by using the list attribute command below:
 
#Ls-lah
 
To add permission to your file use the “chmod” command below:
 
#chmod +x <your file name>

 
4.  File Requirements
Next, I added the following gems to my requirement:
                       
require 'open-uri'
require 'nokogiri'
require 'pry'
require 'colorize'
 
require_relative "./chefilicious_cli_gem/version"
require_relative './chefilicious_cli_gem/meal_kits'
require_relative './chefilicious_cli_gem/cli'
require_relative './chefilicious_cli_gem/chefs'
 
5.  Wring CLI
After I set up my project environments, I was ready to write some code.  

The  following is my initial planning outline:
 
a) My meall kit program will start by greeting the user, and the user will select a key to start the meal kit selection program. 
b) Once the key is selected, Main Menu will appear; 
c) The user will be able to choose the Meal Kit or exit the program; 
d) When the user chooses the meal kit option, 50 best sales meal kits will be listed;  
e) The User can then choose a single meal kit by typing in the number associated with that meal kit and the description from that  meal kit will appear; 
f) When the meal kit description appears, the user can choose the option to click on the web link, which will then connect to the real kit on the website or go back to the main menu to select for another meal kit.
 
6.   Scraping the website
Scraping is no doubt the most difficult and time consuming part of this project.  I greatly appreciated the support I received from the Flatiron School with this part of my project. 
 
I used the following process to build my scraper method:
a) I created a class method of Meal Kits, by using self syntax that refers to the entire class itself.
b) Next, I created an @@all empty array to save instances of the meal kit object.
c) The next step is to grab the desired HTML web page, and parse it using Nokogori to select all elements that are inside < div class > and then iterated over the elements with .each do to get all the instances for my projects.
d)  The final step was to add and save all the components instances to @@all to make a new meal kit.
 
Over all, this project has been fun, challenging, frustrating and rewarding all at the same time. It’s fun and rewarding because planning, creating and implementing a concept can be challenging.  Yet, when you see the final result from your code, it makes your whole experience worthwhile as you come to the realization that “CODING IS SO COOL!”  Simply put, this project give me a glimpse into the boundless  possibilities of coding and I’m loving it!


