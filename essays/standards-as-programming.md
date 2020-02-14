---
layout: essay
type: essay
title: Standards as Programming - Dealing with Human Error
# All dates must be YYYY-MM-DD format!
date: 2020-02-13
labels:
  - Programming
  - Scripting
  - Code Review
  - Program Standards
---

##Small Junkyard Syndrome

Imagine you've been working on something for years. You, and only you, have developed a piece of software, or perhaps a scale model castle, or even a Lego Technic Set. You've created something from the ground up, something from nothing, and you understand how every little mechanism interacts with all the other ones to get the results you want. Variable names are haphazardly thrown together, hallways that exist only for structural support, gears that grind when the motor is running on hi-mode. You understand every detail because you dictated its creation.

Now imagine having to hand that project off to someone else.

This is something I like to call 'Small Junkyard Syndrome.' The work you've done developing this absolute specimen scales poorly if it gets large enough to have to involve someone else. Or even if you go on vacation with parts laying around the office, returning only to realize you don't remember how anything works and didn't bother writing anything down. You've created you own little junkyard of goodies and are top dawg at the pile, but you've limited your creation to only what you can reasonably keep in your head.


##Coding Standards

This whole, return to the mess I created, happened recently when I was going over some code for a Euler Problem that I'd written a forgettably lone time ago.
Look at this section of code and try to figure out what it's doing.

```
public static boolean check(int test){
      int test2 = 0, test3=0, plswork = 2  ;
      for(test2 = 2; test2 < test; test2++){if(test % test2 == 0){return false;}}return true;}}
```

Figure it out? It's to check whether or not a number is prime

Why are there 3 variables named Test?
Why doesn't plswork use camelBack capitalization? Why are test3 and plswork even declared? Why is everything on one line? 

Even the two spaces after ```plswork = 2``` haunts me.

Imagine being gifted a partner such as myself only to realize that you'd have to work with functions that look like the one above? If even a small modicum of Quality Control had been adhered to, this mess would've never been written.

This is the first and most obvious benefits of Coding Standards. Let's say as a partnership we agree to a few simple rules to clean things up.
```1: Declared variables must have a use in their scope. 2: Method and variable names must match their function. And 3: Only one statement per line.```
This is all that's needed to turn the above code into something readable:

```
public static boolean isPrime(int checkThis){
      for(int i = 2; i < checkThis; i++){
         if(test % i == 0){
            return false;
          }
        }
      return true;
   }
``` 

Almost at a glance, you know what everything is doing, why it's there, and can outline what's going on.

##Organization vs. Opinion

This isn't to say Coding Standards have to dictate every keystroke into your IDE. Whether ```i=0``` or ```i = 0``` is correct is for noone but a tyrant to decide. The real choices lie in whether anything can be global, the naming schemes for variables, how to handle user input across your program, or how to balance readability and writability.
There aren't many hard and fast rules that will apply to every software environment, but there are a few generalized goals to want out of any coding standard.

One this is to make things maintainable. Anyone who works with or after you should be able to revisit areas of your code and understand, to the same level that you did, what's going on. This allows projects to be worked on by many people for a long time, meaning you can create bigger, better, and more beautiful programs.

Another is, as the eminent Joel Spolsky puts it ```Look for coding conventions that make wrong code look wrong```. Polymorphism, while interesting in your ICS 111 class, will be a pain to look after if you don't also have all of the variables and methods used at hand to study. Even if you did have them at hand, you'd have to keep all of them in your head while saying one object equals another. The declaration that ```object = new Hammer()``` is easier on the eyes than ```Hammer h = new Hammer(); Tool t = h; Object o = t;```. If there was some malform in your Hammer class being casted down to your Object class, how would you ever know?

A last thing I can think of is to keep human failings in mind. Is your function so long that your opening bracket is 14 mouse wheels away from your closing bracket? Now you and everone before and after you will have to keep those variable scopes in mind while scrolling, good luck with that. Having a big screen is nice, but having a standard that says brackets should be on one screen is smart. 


##Scaling Up

This small junkyard syndrome has to be kept at bay in order for any large organization (anything larger that just you) to create software worth using. Anything created at scale requires the dedicated effort of many programmers and the quickest way to make sure you end up with an unmaintainable mess is to go in with no Coding Standards.