**WDI Fundamentals Unit 10**

---

# Functions and the DOM Cheat Sheet

Here are some notes on what's been covered in this chapter. Feel free to copy this and extend it to make your own cheat sheet.

## Functions

### Defining and Using JavaScript Functions

* A **function** is a custom operation that can be run on command. It can be used both as an operator (accepting input values and calculating output values) and as a subroutine (do this thing, then do that thing).
* Functions must be **defined** before they can be used. To define a function, use the following syntax:

```javascript
var myFunctionName = function() {
  // Body of the function
}
```

* To use, or **call**, a function, simply type the name of your function, followed by `()` (plus any inputs you might be passing in).

```javascript
myFunctionName()
```


### `return` Statements
* In addition to specifying a final value for a function to give back as a result, a `return` statement will cause the function that contains it to immediately end when that line is run. For example, if the function below is operating on a number greater than 10, it will stop executing at its second line and return 15, not `x`.

```javascript
var someFunc = function(x) {
  if (x > 10) {
    return 15;
  }
  return x;
}
```

## Using Functions in the Field

### Best Practices for Writing Functions
* In addition to functionality, making your code readable is one of your most critical considerations.
* Here are some guidelines to keep in mind:
  * Keep your functions small — don't try to do too much in one step.
  * Use good names for functions and variables. Call things what they are!
  * Avoid repetitive code where possible.
  * Generally, don't hard-code specific values into your program if you can help it.


### Problem Solving with Functions
* Sometimes, when you're trying to figure out how to break apart a problem, it can be helpful to imagine the functions that could accomplish specific pieces.
* Learning how to break down a complicated problem into smaller pieces is one of the most important parts of programming, and the best way to get better at it is to practice! In programming, we call this [decomposition](http://en.wikipedia.org/wiki/Decomposition_%28computer_science%29).

## The DOM

* The **Document Object Model (DOM)** provides a structured representation of the HTML document and defines the way it can be accessed by programs to update structure, content, and style.

###Accessing the DOM

* Before we can work with an element, we need to first locate that element in the document. The syntax for searching for an element looks like this:

```js
document.getElementById('main')
```

* Here are the methods that can be used to select an element or elements:

|  Method      |  Description  |
|:-------:    |:-------:|
| `getElementById()`  | Select an element by the value of its `id` attribute. |
| `querySelector()` | Select the first element that matches the provided selector using CSS style syntax.  |
| `document.getElementsByClassName()`   | Select all elements that have a given class name.    |
| `document.getElementsByTagName()`     | Select all elements that have a given tag name.   |
| `document.querySelectorAll()`   | Select all elements that match the provided selector using CSS style syntax.   |

###Traversing the DOM

* Once an element has been selected, this element can be used to select another element based on their relationship. This is referred to as **traversing the DOM**.

|  Property      |  Description  |
|:-------:    |:-------:|
| `parentNode`  | This will locate the parent of the initial selection. |
| `previousSibling` | This will find the previous sibling of a selected element.  |
| `nextSibling`  | This will find the next sibling of a selected element.    |
| `firstChild`     | This will find the first child of a selected element.   |
| `lastChild`   | This will find the last child of a selected element. |

* The syntax for using these properties looks like this:

```js
document.querySelector('li').parentNode
```


###Manipulating the DOM

#### Accessing and Updating Content

* There are several properties we can use to access or update content:

|  Property      |  Description  |
|:-------:    |:-------:|
| `innerHTML`  | Get or set the HTML content of an element. |
| `textContent` | Get or set the text content of an element. |

* The syntax for getting content looks like this:

```js
var firstListItem = document.querySelector('li').innerHTML;
// Remember, querySelector() selects the first element that matches the provided selector.
```

* The syntax for updating content looks like this:

```js
document.querySelector('li').innerHTML = 'Email <a href="mom@gmail.com">Mom</a>.';
```
#### Adding Content

To add new elements to a web page, we'll need to use a three-step process:

1) We will use the `createElement()` method to create a new element that can then be added to the page. When this node is created, it will be *empty*. This element will be stored in a variable.
2) We will then add content to the element using the `innerHTML` or `textContent` properties we looked at in this unit.
3) Now that our element has been created, we can add it as a child of an element using the `appendChild()` method. This will add the element as the last child of the parent element.

```js
var newListItem = document.createElement('li');
newListItem.textContent = 'Feed the cat';
document.querySelector('ul').appendChild(newListItem);
```

####Getting and Setting Attributes
* We can change the value of a class attribute for an element using the `className` property.

```js
document.getElementById('important').className = 'highlight';
```
* We can set and remove attributes from elements using the `setAttribute()` and `removeAttribute()` methods.

```js
document.querySelector('a').setAttribute('href', 'http://newurl.com');
```

```js
document.querySelector('a').removeAttribute('id');
```

###Events
* We can set up **event handlers** in our scripts that will listen, or wait, for an event to occur and then trigger a function.

```js
  element.addEventListener('nameOfEvent', functionToRun);
```
* There are many different types of events we can listen for. Here are a few handlers available to us:

|  Event      |  Description  |
|:-------:    |:-------:|
| 'click'      | When a button (usually a mouse button) is pressed and released on a single element.  |
| 'keydown'     | When the user first presses a key on the keyboard.  |
| 'keyup'   | When the user releases a key on the keyboard.    |
| 'focus'     | When an element has received focus.   |
| 'blur'     | When an element loses focus.   |
| 'submit'   | When the user submits a form.  |
| 'load'   | When the page has finished loading.  |
| 'resize'      | When the browser window has been resized.  |
| 'scroll'      | When the user scrolls up or down on the page. |



---
[Let's put this into practice!](09_assessment.md)
