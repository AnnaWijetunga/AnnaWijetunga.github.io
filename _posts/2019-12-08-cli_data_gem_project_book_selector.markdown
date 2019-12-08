---
layout: post
title:      "CLI Data Gem Project: Book Selector"
date:       2019-12-08 14:46:59 -0500
permalink:  cli_data_gem_project_book_selector
---


Thank you for being here! This project allows any user to select from a list of classic children's book titles, read a short summary and discover the author and informational link for that book. Perfect for any parent who may be overwhelmed by the thousands of books available.

**Why a book selector?**

As a parent myself, I'm often paralyzed by all there is to teach my child. I wanted a program that would allow a parent to quickly search for and grab a book title out of a narrowed down list that every child should have the joy of experiencing.

**Language and skills implemented**

I built this project using Ruby as well as gems Bundler and Nokogiri. My toolset included Visual Studio Code (editor/terminal) and GitHub (to store my repository).

**Feature Highlight** 

This project's beauty is in its simplicity. Each user who interacts with this program is looking for one thing - the next book for their child - and that's precisely what they'll get.

When a user begins, they'll see a narrowed list of classic children's books (52 books). They'll enter the number of a book title that interests them in order to read a 1-2 sentence book summary. 

```
Welcome to Classic Children's Books!
Not sure which of the classics to read to your child next? Take a peek at the list below:

1. "A Apple Pie"

2. “A Princess of Mars,” first in the John Carter series

3. "Aesop's Fables"

4. "Adventures of Huckleberry Finn"
```

From there, they can choose to see the author of the book, as well as a link to more information (publication date, library information), see the book list again or exit the program.

**Hurdles Jumped** 

Let's dig into my main hurdle:

1) Moving my scraper methods to a new file.

Initially, I built my book object to store information about new book instances, but also for my scraping methods. 

In efforts to keep each object to one responsibility, I needed to move my scraping methods to a separate file.

Moving my scraping methods involved a swift copy/paste - not a problem. Calling these methods in my cli file, however, stumped me good.

When I ran my program, no scraped data was displaying. After a great deal of panic and half a day of re-writing methods, editing my logic and testing using binding pry, I finally reached out for help.

And it was then I learned the most important lesson of all:

# Debug following the path of the program.

Credit where credit is due - my cohort lead Chris M. very quickly saw the error and led me to it.

We walked through my cli file and pinpointed exactly where my scraped data was being called but not shown. 

We then searched my scraper file and scanned my methods to see that while I was scraping correctly, data was never being **saved**.

My last line of logic originally called for `book` so I added `book.save`:

```
      book_text = book_node.css("p").to_s # summary
      summary = book_text.split("<br>")[1].strip
      book.summary = summary
      book.save
```

I'd been eagerly barking up the wrong tree - certain that how I'd written my methods for scraping suddenly broke. I learned to follow the path of where my code takes me.

**What's Next**

My ultimate goal was two-fold: to build a program that was relatively functional all along and simple. 

Having accomplished both, I do have a wish-list for when time becomes more abundant:

1) Instead of displaying all 52 books, I'd like to incorporate pagination, such that a user sees 10 titles at a time.

2) I'd like users to be able to read the books in the program. I could link to the site's book reader (have a tab open in a user's browser) or simply add the link to that book.

To see it for yourself, head here: https://github.com/AnnaWijetunga/book-selector-CLI

Thanks so much for reading through! To comment or get in touch, please see the links below. - Anna

Connect with Me [Twitter](https://twitter.com/AnnaWijetunga) [LinkedIn](https://www.linkedin.com/in/annatattan/)
