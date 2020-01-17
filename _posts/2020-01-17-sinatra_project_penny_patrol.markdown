---
layout: post
title:      "Sinatra Project: Penny Patrol"
date:       2020-01-17 16:06:29 +0000
permalink:  sinatra_project_penny_patrol
---

Thank you for being here! 

This project is a Sinatra-powered web application created to track and save expenses. 

**Why an expense tracker?**

As an adult with plenty of bills to pay, I know the weight of worrying about having enough money. This expense tracker was designed for anyone who needs the accountability to see where money is being spent, and this can be the start of taking control of your finances.

**Language and skills implemented**

I built this project using Sinatra and ActiveRecord. My toolset included Visual Studio Code (editor/terminal) and GitHub (to store my repository).

**Feature Highlight** 

This project's beauty is in its simplicity. Each user who interacts with this program is looking for one thing - the accountability of tracking their expenses - and that's precisely what they'll get.

As a new user, you will create an account using a username, email and password. If you've created an account already, you can login using your username and password.

Once logged in, a user will see their expenses. No expenses yet? Click to add. Already added expenses? See your expenses.

A user, if logged in, can add, edit or delete expenses from their tracker. Log out at any time!

**Hurdles Jumped** 

Let's dig into my main hurdle:

Restructuring my params to be in nested hash format.

Initially, I created my params (in all forms as well as all controllers) not in hash format. My project was simple enough, it wasn't necessary.

But! Nested hash format will be important once a project is more complex (hello Rails!), so it was important to me to implement now and get in the habit.

I updated my forms first - here's a snippet (looking at `name =` specifically):

```  <label for="vendor">Vendor: </label>
  <input type="text" name="expense[vendor]" id="vendor"/>

  <br>

  <label for="date">Date: </label>
  <input type="date" name="expense[date]" id="date"/>```
	
Next, the controllers - here's a snippet:

`@expense = Expense.create(params[:expense])`

What I didn't realize was the extent of the update. There were sections I missed entirely because I thought, "Oh this is a quick fix" but didn't slow down to understand what I was updating and why it impacted the entire project.

After a day of breaking, fixing, breaking, panicing, and finally fixing, here's what I learned:
# Errors are your guide.
My soul was weary after I went from perfectly working project to a repeatedly broken project, and every error message I received weighed me down. Until I recognized that they were the key to pointing me in the right direction. Turns out, I was more lost without those error messages than with!

It took a day, a few help sessions, and encouragement from my community, but a day later, I was back to a fully functioning project with nested hash format.

Drop mic.

**What's Next**

My ultimate goal was two-fold: to build a program that was relatively functional all along and simple. 

Having accomplished both, I do have a wish-list for when time becomes more abundant:

1) I want to include goal setting, for folks to describe what they're saving for and track progress.

2) I'd also like to incorporate bootstrap! Having spent a day learning, I realized the potential of how it can transform an app, and I'd like to incorportate that styling to make the app look modern and more user friendly.

To see it for yourself, head here: [GitHub](https://github.com/AnnaWijetunga/budget)

Thanks so much for reading through! To comment or get in touch, please see the links below. - Anna

Connect with Me [Twitter](https://twitter.com/AnnaWijetunga) [LinkedIn](https://www.linkedin.com/in/annatattan/)
