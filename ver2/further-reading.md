## How do we achieve it?

So how can we achieve one `source of truth` in writing HTML?

To achieve one `source of truth` is to say that we would have a template HTML containing our navbar and we would use that template in other pages.

By using pure HTML and CSS, it is possible to achieve such a feat. We can first create a HTML file just for the navbar itself, and then by using `<iframe>`, we can then insert the navbar into another page.

## Do we have another way?

Yes! Fortunately we have multiple ways to achieve this!

The next possible way is to use JavaScript!

## JavaScript to the rescue!

We all know that we can use JavaScript to insert HTML content into a page or to change content in a page.

We also know that we can store `string` or text into a variable.

So we can actually define a function to insert HTML content into different pages!!! All with one function!!! Which means ONE `SOURCE OF TRUTH`!!!

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

## But!!!!

It will be a pain to actually style it, and since its not a conventional way, once you passed on the code to another developer, he/she will have a really bad time.

## Don't really get it?

If you still don't get why you should **not** use these methods. Try making a few HTML pages while also implementing these concepts.
