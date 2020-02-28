---
layout: essay
type: essay
title: Nothing Can be certain
# All dates must be YYYY-MM-DD format!
date: 2020-02-27
labels:
  - Taxes
  - Tax Season
  - UI
  - UI Design
  - UI Frameworks
  - SemanticUI
---

## Except Death and Taxes

As tax season rolls around another year, I prepare to deal with another stack of papers that will serve one purpose for a few days and then spend a lifetime in my filing cabinet. Tax season is never something I look forward to, no matter how many times the IRS decides to add the abbreviation EZ to their 1040 form. 

Naturally this got me thinking about user interfaces and how the work I do to develop a user's environment before the user ever gets there ends up effecting how they treat the entire product. But first, look at the absolute state of this tax form.

<img class="ui center floated rounded image" src="../images/1040EZ.png">

All of these boxes vary greatly in their importance. How many of you reading this actually received tax-exempt interest or qualified dividends? Yet despite this discrepancy in value, visually they're all treated as equals.  The box for your yearly wages receives no more space than the box for social security payouts or capital gains and for descriptions of each box you're told to refer to a different section of the form. It's a mess.

## The interface as programming

The ease of how a potential user interacts with your program will probably determine how many people actually end up using it. As an example, how many of us mailed in or even manually filled out a filed a 1040 this year? Chances are good if you're reading an essay on UI design that you probably used a website that wraps all those messy forms into a neat package that looks something like this:

<img class="ui center floated rounded image" src="../images/TurboTax.png">

While UI and graphical UI aren't normally high ranking in 'coolness' to your average programmer, their implementation can determine whether or not anyone actually chooses to engage with your program. In the case of filing your taxes, we can see how this ease of formatting can influence mass user behaviour simply by looking at the IRS' own statistics on filing:

<img class="ui center floated rounded image" src="../images/E-File.png">

I understand that some other factors are influencing those percentages, such as the increasing prevalence of the internet and people manually E-filing, but just think which one you'd choose. Now imagine the other side of that design. Imagine you're trying to ask people to pay for a piece of software that you've created. Do you think something that looks like the 1040 will have people scrambling to open their wallets? (hint: Intuit, makers of TurboTax, had $6.7B in revenue last year)

## UI design from the maker's end

But a user never has to see how the sausage is made with their websites. They don't have to deal with CSS, html classes, or !important for hours only to produce a website that looks like <a href="http://dancing-baby.net/Babygif.htm">dancing baby</a> or <a href="https://templeos.org">TempleOS</a>.

But then again, neither do we. 

The joy of living in {current year} is that we're able to stand on the shoulders of the giants that came before us. They've already abstracted us away from pure HTML/CSS and given us things like SemanticUI, React, Vue, et al.  These frameworks allow us to replace tomes of css stylesheets with simple phrases that are slipped into the classes of each div. Instead of creating a css that wraps up a paragraph and gives it dynamic edges, box shadows, borders, and menu properties, all we need to do is slap a class="ui container" in there and move on to more important things like figuring out what a <a href="https://www.investopedia.com/terms/w/withholdingallowance.asp">tax allowance</a> is. 

They package common design elements like menus, grids, and transitions into classes that can be applied to any webpage. Which allows us developers to focus on other aspects of our software while also create something that's useful and aesthetically pleasing to the user.

And of this we can be certain, if your website or program is ugly, no one will pay you to use it.
