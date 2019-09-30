# Why you should learn React as a Front End Web Developer

## What is React?

React is a JavaScript library that lets developer create webpages more easily by reducing the amount of lines that developers need to actually write.

---

## How does it work?

JavaScript allows developers to insert HTML dynamically by using

```JS
someElement.innerHTML = '<p>Hello World</p>';
```

If we wrap the line above into a JavaScript function, we can then use it like so.

```JS
const createNavBar = () => {
  document.body.innerHTML += `
  <nav style="background-color: skyblue;">
    <h2>Homepage</h2>
  </nav>
  `
}

createNavBar();
```

So to put it simply, React works by creating HTML elements and inserting them into the page by using methods provided by JavaScript.

---

## How does it makes a difference in your life as a frontend developer?

So why would we use React when HTML, CSS and JS already does the job you may ask.

![meme](https://external-preview.redd.it/TGOVrVeL6z-0TgkiEHevbi7qYbd5BbR6p2Q9r95hOd8.png?width=960&crop=smart&auto=webp&s=11515e5bce4ebe2cf12a3b2d6cb283f68af99183)

Well, we **don't** really have to.

As a developer, we can create wonderful webpages without React, since we can think of it as something that is built from JavaScript, so it is normal to think that JavaScript can do whatever React can do.

It's more about the style of writing it that helps.

## For example

Let's say that we would want to create two HTML pages, a landing page and a profile page with the same navbar by using only HTML and CSS.

index.html
![index.html](example.png)

profile.html
![profile.html](example2.png)

Oh noes!!! The client doesn't like the color of the navbar, he/she wants it to be `#edfaff`. Welp, let's change it then.

index.html
![index.html](example3.png)

profile.html
![profile.html](example2.png)

But whoops we've forgotten to apply our changes to `profile.html` as well!

It's normal for an actual web app to have more than one HTML page, so we might end up missing a page or two when applying changes to the pages.

## Here's where the functions come in

By using the JS code snippet given above as an example, we can create our page as so.

```JS
// index.js
const createNavBar = () => {
  document.body.innerHTML += `
  <nav>
    <h2>Nextagram</h2>
  </nav>
  `
}
```

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
  <body>
    <script src="index.js"></script>
    <script>
      createNavBar()
    </script>
    <!-- Content goes here -->
  </body>
</html>
```

```HTML
<!-- profile.html -->
<!DOCTYPE html>
<html lang="en">
  <body>
    <script src="index.js"></script>
    <script>
      createNavBar()
    </script>
    <!-- Content goes here -->
  </body>
</html>
```

Now we will have 2 HTML pages with the same navbar!

## **Client want's chages to be made again!!!**

**What? You need the background color to be `#fce0ff` this time???**

Fear not! Because this time we only have to change our JavaScript file to make the changes!

```JS
// index.js
const createNavBar = () => {
  document.body.innerHTML += `
  <nav style="background-color: #fce0ff;"> <!-- Add in the style required! -->
    <h2>Nextagram</h2>
  </nav>
  `
}
```

Since both of the pages uses the same function, the navbar created from it will be exactly the same!

**Huh? You need to change the title of the navbar only on certain pages?**

Easy!

```JS
// index.js
const createNavBar = (title) => {
  document.body.innerHTML += `
  <nav style="background-color: #fce0ff;"> <!-- Add in the style required! -->
    <h2>${title}</h2> <!-- Use string interpolation! -->
  </nav>
  `
}
```

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
  <body>
    <script src="index.js"></script>
    <script>
      createNavBar("Nextagram")
    </script>
  </body>
</html>
```

```HTML
<!-- profile.html -->
<!DOCTYPE html>
<html lang="en">
  <body>
    <script src="index.js"></script>
    <script>
      createNavBar("Profile Page")
    </script>
  </body>
</html>
```

This not only makes our lives easier when making changes to our page, but also reduce overall number of lines of code!!!

![meme](https://external-preview.redd.it/TGOVrVeL6z-0TgkiEHevbi7qYbd5BbR6p2Q9r95hOd8.png?width=960&crop=smart&auto=webp&s=11515e5bce4ebe2cf12a3b2d6cb283f68af99183)
