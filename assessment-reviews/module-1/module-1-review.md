# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for? <br>HTML stands for hypertext markup language and is the language used to build web pages.
2. What is the difference between an ID and a class? <br>Class defines the style which is generally done in css file. ID is a way to label parts of the code for referencability.
3. What does it mean to write "semantic" HTML? <br>Writing code where elements have distinguishable roles

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!". <br>
`<p class = "highlight">Watch out!"</p>`
2. Write an HTML image tag to show an image called `profile-picture.jpg`.<br>
`<img src='profile-picture.jpg' />`
3. Write a link tag that links to http://google.com.<br>
`<a href="http://google.com">Link text</a>`
4. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).<br>
```
<DOCTYPE html>
<html>
  <head></head>
  <body></body>
 </html>
 ```
5.Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.<br>
```
<DOCTYPE html>
<html>
  <head></head>
  <body>
    <script src='main.js'></script>
  </body>
 </html>
 ```
6.Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.<br>
```
<DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="main.css">
  </head>
  <body>
    <script src='main.js'></script>
  </body>
 </html>
 ```
7.Write a numbered list in HTML and list three of your favorite books.<br>
```
<ol>
  <li>Of Mice and Men</li>
  <li>Eloquent Javascript</li>
  <li>Lean Startup</li>
 </ol>
 ```
8.Fix the indentation of the following HTML sample:

  ```html
  <div>
  <ul>
  <li>Item 1</li>
    <li>Item 2</li>
  <li>Item 3</li>
    </ul>
    </div>
  ```
<br>
```
<div>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</div>
  ```
## CSS

### Questions

1. What is CSS and what is it used for?<br>
Cascading Style Sheets are a way to define the look of web pages. 
2. What is the CSS box model?<br>
The content of the space of each element including margin, border, padding, and content edges.
3. What's the difference between margin and padding?<br>
Margin controls the space between elements and padding controls space between an element's border and content.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.<br>
    `h1 {
      text-color: red;
    }`
2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  
  ```html
  .btn {
    background-color: blue;
  }
   ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```
  ```html
  .jumbotron {
    p {
      font-size: 20px;
    }
  }
   ```

## JavaScript

### Questions

1. What is a function? What are they used for?<br>
A function is a code set that performs a task and is used to reduce code redundancy.
2. What is the difference between `==` and `===`?<br>
== checks to see if values are equal to each other where === not only checks to see if they're equal but also the same type (e.g. string, number, etc.)
3. What is the difference between global and local scope variables?<br>
local variables live only within the scope of a function where global values can be referenced anywhere
4. What is a boolean value?<br>
Either true or false
5. What is an array?<br>
An object that contains a set of objects under one name

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.<br>
 
 ```html
 var myName = "Melissa Johnson";
 ```
 
2. Write a loop that logs the numbers 1 through 10 to the console.<br>

 ```html
 for (i = 0, i < 10, i++) {
   console.log(i);
 }
 ```
  
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".

 ```html
 score > 3 && lives > 0 ? alert("You win!");
 ```
  
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.<br>

 ```html
 function sayHello(name) {
   console.log("Hello, " + name + "!");
 }
 
 sayHello("Melissa")
 ```
 
5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
<br>
Friday, Friday

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
  <br>
  10

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
<br>
Hello Sarah! Goodbye Sarah!

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.<br>

 ```html
 function findLongestWord(arr) {
  var longestWord = arr[0], x=1;
   
  while (x < arr.length) {
    var longestWord = (arr[x] < longestWord) ? arr[x]: longestWord;
    x++;
  }
  return longestWord.length;
}
  ```
  
9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.<br>

 ```html
 function sum(arr) {
   var sum = 0, x=0;
   while (x < arr.length) {
     sum += arr[x];
     x++;
   }
   return sum;
 }
 ```
 
10.Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.<br>

```html
function vowelCheck(string) {
  var vowels = ["a", "e", "i", "o", "u"], x = 0;
  while (x < vowels.length) {
    if (string == vowels[x]) {
      var result = true;
      break; 
    }
    x++;
  }
    !result ? return false: return result;
}
```

11.Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
  ```javascript
  pet.speak("Charles")
  ```

12.Using the same script as above, write the correct line to log the dogs name to the console.

```javascript
console.log(pet["name"])
```


## Command Line

### Questions

1. What is the command line and what is it used for?<br>
The command line is an interface to the computer operating system or app and allows for submitting commands and receiving responses.
2. What does the command `ls` do?<br>
Lists folder contents (but not hidden files).
3. What does the command `pwd` do?<br>
Stands for `present working directory` and identifies what location (folder) you're currently in.
4. What does the following command do: `cd my-cool-project'<br>
Changes the current working directory to my-cool-project (assuming it exists).

### Exercises

1. Write the command to make a new directory called "my-cool-project".<br>
`mkdir my-cool-project`
2. Write the command to create a file called "index.html".<br>
`touch index.html`
3. Write the command to delete a file called "main.css".<br>
`rm main.css`

## Git

### Questions

1. What is Git and what is it used for?<br>
Git is a version control tool and is commonly used in the developer community to share code.
2. What's the difference between a local repository and a remote repository?<br>
Local respository resides on the users machine where remote is usually located in the cloud.

### Exercises

1. Write the command that you would use to create a new local Git repository.<br>
Type `git init` on the command line from the folder with the name of the repo.
2. Write the command to stage a file called `index.html` to be committed.<br>
`git add index.html`
3. Write the command to view the current status of the git repository.<br>
`git status`
