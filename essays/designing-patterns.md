---
layout: essay
type: essay
title: Designing Patterns
# All dates must be YYYY-MM-DD format!
date: 2020-04-30
labels:
  - Coronavirus
  - Covid-19
  - College
---

# Systems
Whenever a new project is begun, the concern is with systems. What goes where and how you'll put it there lies at the foreground and only later after you've done that a few times do you start to see similar movements being repeated. Maybe you'll be implementing classes that look incredibly similar (declare, access, mutate, etc) and you decide that there should be a system for making these choices more extensible. 

Enter design patterns. When it comes to asking what goes where and how you'll put it there, design patterns asks, who cares? Here's an abstract that will look incredibly similar to that thing you'll have to do over and over again. The concern moves away from individual systems and moves towards creating something that will produce efficient extensible code. 

## Abstractions
Say you've got a television. You've probably got a remote which controls that television with a few buttons on it. When you're a programmer designing that remote, you've got to concern yourself with tracking which channel you're only, state machines that chain together button press, and a whole host of other details that design patterns don't care about. All they care about is what buttons? Your code can be the same. 

When a main method calls a class remote(), we don't necessarily need to see things like remote.buttonPress, remote.backspace, or remote.transmit. These are artifacts leftover from the fact that the person making this started from the ground up and added one thing on top of another.

When it comes to designing patterns, things are viewed the other way round. You first start with an overview of what's necessary and work out from there. The main method will now call a generic remote() command and the remote() class will call each of it's classes internally, simplifying what the other programmers have to interact with. Using this shift in focus, classes can be decoupled, dependecies can be reduced, and you enter a new software project with an idea in mind of how you can apply a generic template or idea first and then move on to implement those patterns line by line.
