---
title: 'Async and Await in Javascript'
date: '2023-01-02'
---

"Async" and "await" are special words in JavaScript that help make your code run more smoothly. Imagine you're making a sandwich and you have to wait for the bread to toast before you can put the peanut butter and jelly on. "Async" is like setting the bread in the toaster, and then telling your computer to go do something else while it waits for the bread to toast. "Await" is like checking on the bread to see if it's done toasting, and then moving on with the sandwich-making process once it is.

Here's an example:


async function makeSandwich() {
    console.log("Putting bread in toaster...");
    setTimeout(() => {
        console.log("Bread is toasted!");
    }, 3000);
    console.log("Doing something else while bread is toasting...");
    }
makeSandwich();


This will log:

> Putting bread in toaster...
> Doing something else while bread is toasting...
> Bread is toasted!

Now, if you want the makeSandwich function to wait for the bread to toast before moving on, you can do:

async function makeSandwich() {
    console.log("Putting bread in toaster...");
    await new Promise(resolve => setTimeout(resolve, 3000));
    console.log("Bread is toasted!");
    console.log("Adding Peanut Butter and Jelly...");
    }
makeSandwich();


This will log:

> Putting bread in toaster...
> Bread is toasted!
> Adding Peanut Butter and Jelly...


So, async and await help you to control the flow of your code and make sure that certain tasks are completed before moving on to the next one.
