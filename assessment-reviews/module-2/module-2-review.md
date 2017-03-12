# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model?<br>
The content of the space of each element including margin, border, padding, and content.
2. What is the difference between block and inline elements?<br>
Block takes up the full width available, with a new line before and after. Inline takes up only as much width as it needs, and does not force new lines 
3. What is responsive design?<br>
Design development should respond to the user environment based on screen size, platform and orientation
4. Which selector is more specific, a tag selector or class selector?<br>
Tag selector is more specific. Tag selectors can be nested within class selectors.
5. What does `box-sizing` do?<br>
Box-sizing alters the default box model. Use this property to emulate the behavior of browsers that do not correctly support the CSS box model specification
6. What's the difference between `relative` and `absolute` positioning?<br>
Relative aligns elements in relation to their parent where absolute has no dependency.

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  
  ```html
  .btn {
    a:hover {
      background-color: blue;
    }
  }
  ```

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  
  ```html
  .container {
    @media (min-width: 1200px) {
      max-width: 980px;
    }
  }
  ```

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  ```
Third paragraph

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.<br>
http://jsbin.com/bisabeyoqe/edit?html,css,output

## JavaScript

### Questions

1. What is a callback?<br>
When a function takes arguments, the callback is an argument that is a function.

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

```javascript
function filterLongWords(arr, num) {
  var newArray = [], x = 0;
  while (x < arr.length) {
    if (arr[x].length > num) {
      newArray.push(arr[x])
    }
    x++;
  }
  return newArray;
}
```

2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

```javascript
function charFreq(string) {
    var freq = {};
    for (var i=0; i<string.length;i++) {
        var character = string.charAt(i);
        if (freq[character]) {
           freq[character]++;
        } else {
           freq[character] = 1;
        }
    }
    return freq;
};
```

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?<br>
DOM stands for Document Object Model. It provides a structured model of the web page so that programs can alter its structure, style and content.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
  ```javascript
  var nextButton = document.getElementById("next')
  ```
  
2. Write another line that updates the text of `nextButton` to `"Next image"`.

```javascript
var nextButton = document.getElementById("next").textContent="Next Image";
```

3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.

```javascript
var nextButton = document.getElementById("next").textContent="Next Image".addEventListener("click", alert("Next image coming up."));
```

## jQuery

### Questions

1. What is a JavaScript library and why do we use them?<br>
A Javascript library is a set of pre-written javascript that allows for faster development of apps. Developers don't need to 'recreate the wheel' and often-used libraries benefit from a lot of use leading to reliability and efficiency.
2. What is jQuery for?<br>
jQuery stands for 'Javascript query' and is one of the most popular Javascript libraries.

### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```
  ```javascript
  var buttons = $(".btn")
  ```

2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

```javascript
var buttons = $(".btn").click(function() {
  alert( "click" );
});
```

## Angular

### Questions

1. How is a framework different than a library?<br>
A library offers multiple predefined functions that a developer can call to improve and expand their application, whereas a framework describes the structure of the application and gives the developers a way to organize their code to make their app more flexible and scalable
2. What is a controller?<br>
In the MVC environment, the controller controls app logic flow between models and views.
3. What is a view?<br>
Usually html code that renders what users see.
4. What is a single page application?<br>
An application that provides the same experience as a multi-page application but relies on non-repeating code to vary the user experience.
5. What is a directive in Angular?<br>
Directives are markers on a DOM elementthat tell AngularJS's HTML compiler to attach a specified behavior to that DOM elemen (e.g. event listener).

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.<br>
`git checkout -b bug-fix`
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
`git merge bug-fix`
