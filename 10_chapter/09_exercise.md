**WDI Fundamentals Unit 10**

---

##![Your Turn](../assets/exercise.png) Your Turn

Below is the starter code for your next exercise. If you don't see the JS Bin, please refresh the page.

<a class="jsbin-embed" href="http://jsbin.com/guvuva/1/embed?html&height600">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.35.12"></script>

In this exercise we're going to practice manipulating the DOM by updating our "Reading List" site, which is a little outdated.

For now, we'll run our JavaScript to update the DOM when the page loads. In the next lesson we'll take a look at how we can update the page based on a user's actions; maybe we'll add a list item when the user clicks on a button. Or, perhaps we'll remove a list item when the user clicks on an `X` icon.


###Instructions

1) Let's get started! Some starter code has been provided in the JS Bin for this exercise.
2) Write the code to perform the actions listed below in the "JavaScript" panel.
3) Click "Run" to see the results in the "Console" panel.

**Let's get started!**

* Use the `querySelectorAll()` method to select all elements with the `current` class. Using array syntax (our trusty square brackets), find the second element with the `current` class, and update the text content to "Me Talk Pretty One Day."

* Use the `getElementById()` method to find the element with the ID `next`. We want to add a link to this book so we can purchase it. Change the inner HTML of this element to include an anchor: `<a href="http://www.amazon.com/Flamethrowers-Rachel-Kushner/dp/1439142017/ref=sr_1_1?ie=UTF8&qid=1458897183&sr=8-1&keywords=the+flamethrowers">The Flamethrowers</a>`.

* Find the first `li` using the `querySelector()` method. Change the inner HTML to `The Wind Up <strong>Bird</strong> Chronicle`.

* Find the fourth list item using the `querySelectorAll()` method. Change the text to "I'm the fourth!"

* Use the `getElementsByTagName` method to select all `li` elements. Then, use a `for` loop to iterate through these elements and change the text content to "JavaScript rules!"

* Use the `getElementsByClassName` method to select all elements with the `current` class. Then, use array syntax to select the first item from that class and change the inner HTML to "Manipulating the DOM is fun!"



---

Nice work! [Now, let's dig in a little deeper.](10_lesson.md)
