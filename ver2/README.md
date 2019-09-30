# React

## Problem Statement

Let's assume that we are asked by our client to create 10 pages of content in the company's website, all with the same navigation bar.

We proceed to design the navigation bar and placed them into 10 different pages.

Here are some example.

index.html
![index.html](../ver1/example.png)

profile.html
![profile.html](../ver1/example2.png)

**\*Phone rings**

Oh noes, the client wanted the color of the navigation bar to be changed to `#edfaff`.

## Welp, let's get to work then.

We proceed to change the color of the navigation bar and replaced the navigation bar in the pages.

index.html
![index.html](../ver1/example3.png)

profile.html
![profile.html](../ver1/example2.png)

**\*Client called again!**

Whoops!! Apparently we have forgotten to apply the change to few of the pages.

---

Accidents like this happens all the time, as a website is always comprised of many HTML pages. We are not perfect human beings, making mistakes here and there is perfectly normal!

---

## Solution

One of the solutions is to only have one source of truth.

## Source of truth

So what do I mean by `one source of truth` you asked?

For now every page of HTML we have, we will have a navigation bar for it. Since changing the navigation bar of one of the page will not change the rest, we can say that they are from a seperate source of truth.

## Head's up!

By using only HTML or combining it with JavaScript, it is entirely possible to implement the concept of one source of truth, but it's not a common practice to do it and it has some drawbacks as well. Further reading over [here](further-reading.md)!

## What is React?

First I would need to explain what is React.

React is a frontend framework that is built on JavaScript, basically speaking it's just a bunch of functions and code written in JavaScript, the main purpose of these code is to make developer's live easier by solving the above problems and more.

How React works is similar to what we discussed above. A developer would first define a HTML template in JavaScript, that template will be what we call a `component`.

```
You can think of it as a abbreviation for a bunch of HTML, very cool right?
```

The said `component` can be used in anywhere, even in other `component`s.

## To solve the current problem we're facing.

A template of our navigation bar can be defined in our `component`, and then the `component` can be used in multiple pages.

Although some setups are still required for React, but after all that you can use the defined component like so.

```HTML
<body>
  <MyNavBar /> <!-- This is the abbreviation mentioned -->
</body>
```

## Do we need to learn React?

Technically speaking, you **don't**!

As mentioned, React is built on JavaScript. That means whatever React is capable of achieving, JavaScript can do the job too!

So why do we prefer React over Vanilla JavaScript?

## Write less, do more.

## Decrease development time, increase productivity.

React offers reusable `component`s, that means that the HTML that we write in React are all potentially reusable, thus reducing amount of code needed significantly.

```
It feels like printing a document on a printer, all the papers that are printed out follows a single source of truth that is the document on your device. Compared to writing the papers all by hand, which might also cause discrepancy between the papers.
```

---

### Hey!!!

Are you worried about what if we need to tweak the `component` in one of the page but not the rest?

Fear not! As `component`s are just templates, we can customize it when we are actually using it. For example a `component` of a navigation bar by default has a white color background, but we can change that one particular navigation bar's background color to skyblue.

```
You can treat a fried rice recipe as a component. You can keep on cooking 10 of the same dish, or you can also spice it up by adding a bunch of hot sauce in one of the plates.
```

---

## More organized code, faster debugging time.

React also allows easier logic implementation, for example if we have a email input field that needs to be checked for a valid email, its logic can be easily be contained in one `component`, and then be reused whenever we need it.

Logical bugs can also be tracked down fairly easily. If a `component` isn't behaving as it should, since all logics for a `component` is contained within one single file, the bug can be found within a short amount of time.

```
It's like organizing seasonings, utensils, and cookwares into their own cabinet so that it's easier to find them.
```
