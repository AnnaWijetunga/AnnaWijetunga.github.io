---
layout: post
title:      "MVC - Framing Sinatra"
date:       2019-12-20 21:47:10 +0000
permalink:  mvc_-_framing_sinatra
---


Digging into Sinatra has introduced me to a critical concept - the Model-View-Controller framework. Sure seems like it's here to stay - let's talk through it.

The **Model-View-Controller** framework is the foundation upon which a program can fluidly operate as a web application. 

To really drive this home, I'd like to expand upon Flatiron's restaurant analogy (kudos to Flatiron for the intro!).

**Models**

Imagine - it's date night and you've just sat down to dinner at [insert your favorite restaurant]. While you likely can't see him/her, you know the chef's in the kitchen.

Your waiter (finally) comes to take your order. Now the moment you've waited for - the waiter brings your order back to the chef, who prepares your meal. 

As soon as it's ready, the chef passes your plate to the waiter, who brings it directly to you. Bon appetite!

Now I'm hungry, but back to Sinatra. Models are the logic behind your application - and your **chef** is the **model** here. Your chef took your order from the waiter, prepared your meal, and gave it to your waiter. Your chef manipulated/created your food, and the models manipulate data.

**Views**

You place your order with your waiter. While you sip your fancy adult beverage, your waiter takes your order to the kitchen, and soon enough, you receive your meal. This meal, the food, is the **view**.

In Sinatra, views are what the user sees and the only part that the user interacts with directly. Views are written as `.erb` files. They consist of HTML and embedded Ruby, which is code written within HTML.


**Controllers**

Your waiter is the **controller**, the go-between for the kitchen and you. Your waiter takes your order from you to the kitchen. And, they take meals from the kitchen to you.

In Sinatra, controllers are the go-between for models and views. Controllers have routes. These routes take requests sent from the browser, run code, and then render the `.erb` (view) files for the user to see.

This MVC concept separates an application's code by function. Reason being, this makes writing, reading and even debugging code far more simple and far more pleasant.

So they say! I'll keep digging in and report back, but that's for now I'll take their word.

Connect with Me [Twitter](https://twitter.com/AnnaWijetunga) [LinkedIn](https://www.linkedin.com/in/annatattan/)




