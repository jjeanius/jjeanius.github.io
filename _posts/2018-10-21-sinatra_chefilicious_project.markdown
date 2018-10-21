---
layout: post
title:      "Sinatra Chefilicious Project"
date:       2018-10-21 18:10:33 +0000
permalink:  sinatra_chefilicious_project
---


#Even though the meal kit market has only been around for a few years, business is booming.  While there were initially only a handful of companies, now the industry is growing, due to acquisitions by large retail companies; and many of these companies now market these well-known meal kits locally in their stores, thus fueling rapid expansion.  Revenue is expected to hit $10 billion dollars by 2020.  

I like meal kits because they provide healthy meal choices delivered directly to your door with all the necessary ingredients included; no need to battle the crowds at the supermarket.  
To order meal kits, you simply go to the company’s website, select the desired recipe(s), confirm your order, and the product is shipped directly to you, along with the necessary instructions and the premeasured ingredients.   In a nutshell, this is one stop, or should I say “no stop”, shopping at its best.

I incorporated the meal kit concept into my Sinatra application because I like the concept and the idea.  

I begin my project by using a gem called “corneal” to generate a Sinatra template.  It is a Sinatra application generator allows you to easily start building your Sinatra with all the required gems.   

I organized my code in MVC structure (Model, View, Control), because it makes working and revisiting my codes much easier and cleaner.   

For database:   I decided to work with only 2 tables:  a “customers” table and a “mealkits” table.  

For model:  I created a “customers” model and  a “mealkits” model.   The relationship between them will be one to many relationships; A customer has many meal kits and a meal kit belongs to a customer.  

I created 3 controllers in the app, they are:  ApplicationController, CustomerController, and MealkitController.  Their main functions are to go-between the models and the views by using ‘routes’ that take requests sent from the browser, run the code and then render the erb views. 

The final part of the component is the views.  Since view is the “front-end, user facing part of the web application, I organized it in 2 folders:  a	"customers" folder, and a "mealkits" folder.  The ruby files in these folders will perform CRUD actions.

Finally, mounting all 3 controllers in the config,ru file are necessary, because we need to let Rack know the controller part of the application is defined within our controller classes.  Here is the finish product:  
![](https://imgur.com/a/lkrueO3)


As a final word, despite its complexities and challenges, I enjoyed working on this Sinatra project.   This project is a continuation of my first CLI project for many reasons; I like the meal kits concept and I really believe you can create, modify a comprehensive app that target this growing industry. 

Over all, I think this project allowed me to put my learning and my knowledge into practice.  As for my app, I can envision this app helping a company keeping track of orders, inventory and even sales.  One of the advantages of this application is its flexibility so there is still room for improvement, and I’m really looking forward to all of the good improvement that I will make as my study continue. 


