# React

## Problem Statement

Let's assume that we are asked by our client to create 10 pages of content in the company's website, all with the same navbar.

We proceed to design the navbar and placed them into 10 different pages.

Here are some example.

index.html
![index.html](../ver1/example.png)

profile.html
![profile.html](../ver1/example2.png)

**\*Phone rings**

Oh noes, the client wanted the color of the navbar to be changed to `#edfaff`.

## Welp, let's get to work then.

We proceed to change the color of the navbar and replaced the navbar in the pages.

index.html
![index.html](../ver1/example3.png)

profile.html
![profile.html](../ver1/example2.png)

**\*Client called again!**

Whoops!! Apparently we have forgotten to apply the change to few of the pages.

---

Accidents like this happens all the time, as a website comprise of many HTML pages. We are not perfect human beings, making mistakes here and there is normal!

---

## Solution

One of the solutions is to only have one source of truth.

## Source of truth

So what do I mean by `one source of truth` you asked?

For now every page of HTML we have, we will have a navbar for it. Since changing the navbar of one of the page will not change the rest, we can say that they are from a seperate source of truth.

### How do we achieve it?

So how can we achieve one source of truth in writing HTML?

To achieve one source of truth is to say that we would have a template HTML containing our navbar and we would use that template in other pages.

By using pure HTML and CSS, it is possible to achieve such a feat. We can first create a HTML file just for the navbar itself, and then by using iframe we can then insert the navbar into another page.

## But!!!!

It will be a pain to actually style it, and since its not a conventional way, once you passed on the code to another developer, he/she will have a really bad time.

## Do we have another way?

Yes! Fortunately we have multiple ways to solve this problem.

The next possible solution is by using JavaScript!

## JavaScript to the rescue!

We all know that we can use JavaScript to insert HTML content into a page or change the content in a page.

We also know that we can store `string` or text into a variable.

So we can actually define a function to insert HTML content into all 10 pages!!! All with one function!!! Which means ONE SOURCE OF TRUTH!!!

```JS
function createNavBar() {
  document.body.innerHTML += "<nav></nav>"
}
```

```HTML
<html>
  <head>
    <script src="index.js"></script>
  </head>
  <body>
    <script>
      createNavBar()
    </script>
  </body>
</html>
```

## But wait!!! What about React then?

The title of this blog post is about React, but after all these explanations and examples, the word React did'nt come up even once, what's going on?

## What is React?

First I would need to explain what is React.

React is a frontend framework that is built on JavaScript, basically speaking it's just a bunch of functions and code written in JavaScript, the main purpose of these code is to make developer's live easier by solving the above problems and more.

How React works is similar to what we discussed above. A developer would first define a HTML template in JavaScript, that template will be what we call a `component`, the said `component` can be used in anywhere, even in other `component`s.

## Since we already have the above solution, why do we still need React then?

Technically speaking, you **don't**!

As mentioned, React is built on JavaScript. That means whatever React is capable of achieving, JavaScript can do the job too!

So why do we prefer React over Vanilla JavaScript?

React offers reusable `component`s, that means that the HTML that we write in React are all potentially reusable, thus reducing amount of code needed significantly.

## Write less, do more.

## Decrease development time, increase productivity.

React also allows easier logic implementation, for example if we have a email input field that needs to be checked for a valid  email, its logic can be easily be contained in one `component` then be reused whenever we need it.

Logical bugs can also be tracked down fairly easily. If a `component` isn't behaving as it should, since all logics for a `component` is contained within one single file, the bug can be found within a short amount of time.

## More organized code, faster debugging time.
