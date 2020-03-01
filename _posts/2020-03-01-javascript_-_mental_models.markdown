---
layout: post
title:      "JavaScript - Mental Models"
date:       2020-03-01 17:15:46 +0000
permalink:  javascript_-_mental_models
---


After three months of Ruby, JavaScript hit me like a brick wall. Two weeks in and I had to slow down and find my bearings.

Flatiron's curriculum has always been exceptional, but it always helps to hear it again, in different ways.

I signed up for Dan Abramov's hot new course, Just JavaScript, and one of the early lessons made a huge impact.

Dan shares a bit about slow and fast thinking from author Daniel Kahneman:

> Whenever we can, we rely on the “fast” system. We share this system with many animals, and that gives us amazing powers like walking without falling all the time. This “fast” system is good at pattern matching (necessary for survival!) and “gut reactions”. But it’s not good at planning.
> 

Because slow thinking can be so draining, we mere humans default to fast thinking. And this gets us into trouble because we may miss bugs in our code.

The "fix" here is to pay attention to, and in a newbie's case, **build** our mental models.

```
let a = 10;
let b = a;
a = 0;
```

Our mental model would be how we talk through and understand code. 

For example:

```
let a = 10;
Declare a variable called a. Set it to 10.

let b = a;
Declare a variable called b. Set it to a.
Wait, what’s a again? Ah, it was 10. So b is 10 too.

a = 0;
Set the a variable to 0.
So a is 0 now, and b is 10. That’s our answer.
```

While rushing through labs and lessons always seems important to stay on track with the curriculum, I know that slowing down my thinking to ensure I'm building my own mental models is actually the priority. Tis a work in progress but this time, in the right direction.

