---
layout: essay
type: essay
title: Real Questions - How what you ask reflects on who you are.
# All dates must be YYYY-MM-DD format!
date: 2020-01-30
labels:
  - Questions
  - Answers
  - StackOverflow
---

## Questions as an escalation

"We hired you to troubleshoot, not to ask us to do your job."

Questions shouldn't serve as an initial step, they should be escalating an already in progress train of thought. Showing others that you can not only think, but act, by yourself towards the solution of a problem will not only win you the guidance of an answer, but also the respect of your peers. Or at the very least, prevent from being ostricized.

When a problem is presented and the solution isn't clear, the first step should be to tinker. How does changing the input effect my programs output? Where in my program does it stop doing what I want it to? If I replace this part in my computer, will it produce a different error? This tinkering allows you to not only discover where a problem is coming from, but it allows you to learn more about the system that you're interacting with.

Questions comes into play afterwards, once all of your internal struggle has been exhausted and you're in need of either a new direction or a puzzle piece that isn't attainable on your own. How you ask these questions reflect more on who you are that you might realize.


## Real Questions

If the potential question asker has followed thru the tinker and exhaust steps, they're next stop is usually the internet. A quick google search here and there will either give them the information they need to soldier on after querying a few keywords, or they've discovered that their problem is a little more unique and might need the additional assistance of another technician.

```
A related question has been answered here.

My query is, following approach-1 works, however the variation of it, that is approach-2 does not, rather
it gives double the value of expected output. I can not find out why.

Approach-1
public class Solution {
    public int numSetBits(long a) {
        int count = 0;
        long temp = 0;
        for(int i = 0 ; i < 64 ; i++) { // 64-bit for long data-type
            temp = 1;
            temp = temp << i;
            temp = a & temp;
            if((temp > 0))
                count++;
        }
      return count;
    }
}

Approach-2
public class Solution {
    public int numSetBits(long a) {
        int count=0;
        for(int i=0; i<64; i++) {
            if((a & (1 << i))>0) count++;
        }
      return count;
    }
}
```

This question is very real in the sense that this isn't the asker approaching his audience with nothing in hand. He's sought his own answers and tinkered around with the problem before realizing that there might be something he isn't privy to that might be stopping his solution.

The answer is no slouch either

```
The second approach fails because the result of 1 << i is an int, not a long. So the bit mask wraps around, 
and so the lower 32 bits of a get scanned twice, while the higher 32 bits of a are left uncounted.

So, when i reaches the value 32, (1 << i) will not be 232, but 20 (i.e. 1), which is the same as when i was 0. 
Similarly when i is 33, (1 << i) will not be 233, but 21, ...etc.

Correct this by making the constant 1 a long:
(1L << i)
```

The solution to the askers question did indeed contain information that wasn't even in the same ballpark he was batting in. But the fact that he was on the path of solving his own problem and treated his question as an escalation of an existing thought process gave the community around him not just a sense of who he was, but also a lower level understanding of why their programs behave the way they do.


## Hollow Minds

Poor questions on the other demonstrate a persons lack of participation in the troubleshooting process. These are people who have contributed no thought, no effort, and no enthusiasm to the problem they're facing.

The question reads:

```
Is it possible to use CardView with RecyclerView and NavigationDrawer all together? If it is possible, 
someone suggest me any example based on it, and if it is not possible, then pls give me an 
answer explaining why it is not possible?

For example, if in this sample code given in this url: http://javatechig.com/android/android-recyclerview-example, 
I want to add a DrawerLayout simultaneously with RecyclerView and CardView, then is it possible or not ?????

Thanks in advance
```

Here we have a user who cannot be bothered to google. They can't even be bothered to consult the dev docs or youtube videos that would give them the overarching view that would answer their question. They've brought nothing to the community and demanded answers by posting this question.

And the answers here pick up on his slouch.

```
Take a look here android-developers.blogspot.in/2015/05/….. And chris banes has shown a 
wonderful example of its application take a look here github.com/chrisbanes/cheesesquare – George Thomas
```
And his response:
```
Thank you for the example but just have query is it possible to collabrate all 3 views without 
using collapsingtoolbarlayout as used in example like its possible to collabrate recycleview and
cardview at a time in the same manner recycleview+cardview+navigationdrawer at a time
```

Another potential answer?
```
Yes, it is certainly possible to use cardview with recycleview and navigationdrawer.

You can view the following:

Getting Started With RecyclerView and CardView on Android
Material Navigation Drawer with recycle view and Card view
RecyclerView in Material Design
If you want a video, I would recommend watching:

Android Material Design Tutorial -- Slidnerd
He really explains it very well in this series. You can also find many others on YouTube.
```
And a predictable response:
```
Thanks for URL but i already tried recycle with cardview or recycle with navigation drawer but 
dont get all 3 together and that video is not in working :)
```

Not only though their question, but also their engagement with the community has this person demonstrated their disdain for search. They've posed a question and when given the response that the information has been posted in superior formats, they demand that the anser'ers rechew the information into something he prefers.


## Thoughts from a Lead Technician

The field I work in is a revolving door. Technicians come and go, new ones take their place, very little 'lingers'. One common thread among all of them is how they choose to ask for help when a new or particularly challenging problem comes up. The juxtaposition of Goofus and Gallant comes to mind.



Gallant will ask questions about how the problem arose, goofus will ask specifically what error is being received.

Gallant will play around with the error until he has informed ideas about it, goofus will stop as soon as he comes across something he's never seen before.

Gallant will consult the knowledge base articles, test the problem from various angles to know exactly where the issue is, and only discovering the broken link in the chain ask you, "Who is the appropriate party to escalate this issue to?"

Goofus will have done nothing, come to you with nothing, and demand that his problem become your problem. Usually in the form, "Users are having this issue, how do I fix it?"



Who would you rather work with?
