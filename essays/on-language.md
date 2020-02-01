---
layout: essay
type: essay
title: On Language
# All dates must be YYYY-MM-DD format!
date: 2020-01-31
labels:
  - Binary
  - Thoery of Computation
  - JavaScript
---

## The Language of Computers

```
0101010001101000011010010110111001101011001000000111100101101111011101010010011101110010011001010010000001100011011011000110010101110110011001010111001000111111
```

	Confused? As it should be unless you're an electrical box that crunches digits all day. The binary we're seeing is simply data that's being represented in a way that can be understood to a computer. Typically, that computer is modeled under what's known as a Von-Neumann architecture, but that's a conversation for another time.
	These bits are the lowest form of communication (low as in closest to the computer hardware without being actual hardware) that we have with computers and also the way all of our code words are broken down and fed into computers.



## The Language In-between

	  But what if we don't want to communicate with numbers using 1's and 0's? What if we'd like to type a number or letter into a terminal and have the computer understand on a binary level what we're entering?
	  Well first we'd have to all agree on a way to count (00000001=1, 00000010=2, etc) and perhaps a table of numbers (10000001=a, 10000010=b, etc) and now we'd have a natural way to type into these magic boxs and program them to our liking. In this one simple step we've managed to take the binary data that is fed into computers and wrap/conceal them underneath a letter of our keyboards. We've abstracted a layer away from the computer and made things easier to understand for the human using it.

  Why don’t we take this a step further?



## Functions as Words

	Take the benevolent for loop. Contained within it you’ve got a couple of letters and maybe a number, a comparison operator, and a block of code.
```
for ( let i=0; i<intArray.length()-1; i++ ) {
	System.out.println(intArray[i]);
}
```
	But you’ve actually got so much more than that if you translate that into the lower level implementation. After each word is broken down into component letters. If we’ve already described to the computer what a for loop looks like in letters and the rules it should use when presented with those letters. It will translate the F, O, and R, into it’s appropriate binary representation, and treat the following binary-translated code (the for loop conditions and the code block) accordingly.
	This method of wrapping binary as letters, letters as words, and words as functions can continue to be abstracted. With each abstraction away from bit-level binary, the code takes a little longer to translate into something the computer can understand, but also allows us to create higher and higher level functions that would be infeasible in other languages.


## High Level Languages
	
	So, let’s say we continue this pattern of wrapping up repetitive functions and representations into something simpler for us meat bags to understand. Where does that get us?
	Binary gets concealed into machine code, which gets concealed into assembly code, which gets concealed into middle/high level languages, which get concealed in script languages.
	To make a long story short, JavaScript is where we’re at with this method of abstracting away from the computer. We don’t have to type in any 1’s or 0’s, we don’t have to write in hexadecimals, and we don’t even have to typecast our variables when we declare them. Being so far away from the machine, this language becomes so readable to humans, bordering on pseudocode, that we can create incredibly complex systems that are just impossible lower on down the chain. Things like returning a function instead of a variable, data structures that exist in higher dimensions, and notations that allow us to solve complex problems in much fewer lines.
	The clever reader has probably noticed a slight downside to all this wrapping. Wouldn’t it take a while to unwrap your way all the way down to where the computer actually does things? Yes, yes it does. But if we truly cared about compile or run times then we’d use a language that’s made for that. The use of higher level scripting languages is in their ease of use and compressibility, which doesn’t exist anywhere lower down the chain.



## The new Long() and new Short() of it all

	Each language at every step of the chain is, by grace of abstraction, useful for different things. Want to make a driver that interoperates your graphics card with the rest of your computer? Used assembly. Want to make an Operating System? Use C. Want to design a website or make a usable program? Use Javascript.
	Each of their existences at different levels of the abstraction pyramid justifies each of their use cases without mandating a debate on which one is the best.
	The fact that this process of hiding implementation details in higher level forms has been going on for decades before we came along is something worth celebrating.
