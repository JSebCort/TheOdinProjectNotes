# Fundamentals Part 1

## Knowledge Check
1. Name the three ways to declare a variable?
    * You can use either 'const', 'let' or 'var' to declare a variable.
2. Which of the three variable declarations should you avoid and why?
    * You should avoid using 'var' as 'let' and 'const' are the new ways of declaring variables in the latest versions of JavaScript.
3. What rules should you follow when naming variables?
    * You should use camelCase when declaring variable names with multiple letters (i.e. myVeryLongVariable)
    * You cannot have a digit be the first character of a name and symbols other than '$' and '_' are not allowed.
    * The words 'let' and 'return' are reserved and cannot be used as a variable name.
    * Named constants, that are hard-coded, are often named in capital letters and underscores. (i.e. const COLOR_RED = "#F00") 
4. What should you look out for when using the + operator with numbers and strings?
    * If you try to use the + operator on a string and a number, it will instead concatenate the two as if they were both strings. (i.e. '1' + 2  = "12")
    * Using the + operator on two numbers and then a string, it will add the numbers together but concatenate the sum with the string. (i.e. 2 + 2 + '1' = "41")
5. How does the % operator work?
    * % is the remainder operator, also known as modulo.
        * It will produce the remainder of a division between two numbers.
        * i.e. 10 % 3 = 3 Remainder 1. So this operation returns 1.
6. Explain the difference between == and ===.
    * Loose/Abstract Equality (==) compares equality after doing any necessary type conversions.
        * i.e. '17' == 17 returns 'true' as the '17' is converted into a number and is then compared. 
    * Strict Equality (===) compares equality without any type conversion.
        * i.e. '17' === 17 returns 'false' as the two operands being compared are not of the same type.
7. When would you receive a NaN result?
    * You utilize either the '++' operator to increment a number or the '--' operator to decrement a number.
8. Explain the difference between prefixing and post-fixing increment/decrement operators.
    * The prefix form ('++variable') will return the new value after increment while the postfix form ('variable++') will return the value before the increment.
    * Prefix Form
        ```js 	
        let counter = 1;
        let a = ++counter; // (*)
        alert(a); // 2
        ```
    * Postfix Form
        ```js
        let counter = 1;
        let a = counter++; // (*) changed ++counter to counter++
        alert(a); // 1
        ```
9. What is operator precedence and how is it handled in JS?
    * Operator precedence is what determines which order operators are handled.
    * Exponentiation has a precedence value of 16 while addition has a precedence value of 13. As a result, an exponent will be handled before the addition.
    * [Precedence Table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#table)
10. How do you access developer tools and the console?
    * Right-Click on a page, select 'Inspect Element' and click on the 'Console' tab within the developer tools.
    * Using the 'Ctrl + Shift + I' or 'F12' shortcuts.
11. How do you log information to the console?
    * Using 'console.log()' within the HTML file will cause information to be logged within the console.
12. What does unary plus operator do to string representations of integers?
    * Unary plus operator will convert the string representation into a number.
    * Example without unary plus

        ```js
        let apples = "2";
        let oranges = "3";
        alert( apples + oranges ) = 23
        ```
    * Example with unary plus

        ```js
        let apples = "2";
        let oranges = "3";
        alert( +apples + +oranges ) = 5
        ```	
# Fundamentals Part 2
## Notes
1. Eight basic data types in JavaScript:
    * Number - Integer and floating-point
    * BigInt - Integer values larger than [2^53]-1, or 9007199254740991, and less than -[2^53]-1 for negatives
    * String - You can utilize double quotes (""), single quotes ('') and backticks (``)
        * Backticks allow the ability to embed variables and expressions into a string by wrapping them in ${…}
            ```js
            let name = "John";

            // embed a variable
            alert( `Hello, ${name}!` ); // Hello, John!

            // embed an expression
            alert( `the result is ${1 + 2}` ); // the result is 3
            ```
    * Boolean - True and false values
    * null value - Special value that represents “nothing”, “empty” or “value unknown”.
    * undefined value - Special value that represents "value is not assigned"
    * Object and Symbol - Objects are used to store collections of data and other complex entities. Symbols are used to create unique identifiers for objects.
2. typeof operator returns the type of the argument
    ```js
    typeof undefined // "undefined"
    typeof 0 // "number"
    typeof 10n // "bigint"
    typeof true // "boolean"
    typeof "foo" // "string"
    typeof Symbol("id") // "symbol"
    ```		
3. A number 0, an empty string "", null, undefined, and NaN all become false. Because of that they are called “falsy” values. Other values become true, so they are called “truthy”.
	* In JavaScript, a truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN).
        ```py
        # Written in python
        a = 5
        if a:
            print(a) # Gives an output
        a = 0
        if a:
            print(a) # Doesn't give an output
        ```	
4. Conditional (ternary) operator:
	* The only JavaScript operator that takes three operands.
	* A condition followed by a question mark (?), then an expression to execute if the condition is truthy followed by a colon (:), and finally the expression to execute if the condition is falsy.
	* Frequently used as a shortcut for the if statement.
        ```js
        function getFee(isMember) {
            return (isMember ? '$2.00' : '$10.00');
            }

        console.log(getFee(true));
        // expected output: "$2.00"

        console.log(getFee(false));
        // expected output: "$10.00"

        console.log(getFee(null));
        // expected output: "$10.00"
        ```
## Knowledge Check
1. What are the eight data types in JavaScript?
    * Number, BigInt, String, boolean, null, undefined, Object and Symbol.
2. Which data type is NOT primitive?
    * Object.
3. What is the relationship between null and undefined?
    * 'null' is an assigned value that means 'nothing' while 'undefined' is a declared variable that hasnt been defined. So 'null === undefined' is false but 'null == undefined' is true.
4. What is the difference between single, double, and backtick quotes for strings?
    * All three can be used to define strings but backtick allows for embedded variables and expressions.
5. What is the term for embedding variables/expressions in a string?
    * Wrapping
6. Which type of quote lets you embed variables/expressions in a string?
    * Backticks
7. How do you embed variables/expressions in a string?
    * ${..}
8. How do you escape characters in a string?
    * Utilize the backwards slash (\) character such as 'I\'ve got no right to take my place...'
9. What are methods?
    * They are actions or functions that are performed on objects. 
10. What is the difference between slice/substring/substr?
	* Slice returns parts of string given indexes. Such as the slice of a string from index 1 to 10, the slice starting from index 5 or the slice counting from the end of the string.
        ```js
        let str = "Apple, Banana, Kiwi";
        let part = str.slice(7, 13); // Banana
        let part = str.slice(-12, -6); // Banana
        let part = str.slice(7); // Banana, Kiwi
        let part = str.slice(-12); // Banana, Kiwi
        ```
	* Substring is similar to slice but cannot accept negative indexes).
        ```js
        let str = "Apple, Banana, Kiwi";
        let part = substring(7, 13); // Banana
        ```
	* substr is similar to slice but the second argument isn't for the ending index, rather the number of positions after the starting index that the returning string will be.
        ```js
        let str = "Apple, Banana, Kiwi";
        let part = str.substr(7, 6); // Banana
        ```
11. What are the three logical operators and what do they stand for?
	* OR (||)
	* AND (&&)
	* NOT (!)
12. What are the comparison operators?
	* Less Than (>) and Greater Than (<)
	* Less Than or Equal To (>=) and Greater Than or Equal To (<=)
	* Equal To (==) and Not Equal To (!=)
13. What are truthy and falsy values?
    * Falsy values (such as 0, NaN, undefined, etc.) become 'false' when checked. Other values become 'true'.
14. What are the falsy values in JavaScript?
    * 0, an empty string "", null, undefined, and NaN
15. What are conditionals?
    * Conditionals control whether or not pieces of the code are run. Conditionals include 'if', 'else', and 'else if'.	
16. What is the syntax for an if/else conditional?
	```js
    if(10>5){
        alert("Hello!");
    } else{
        alert("Goodbye!");
    }
    ```
17. What is the syntax for a switch statement?
    ```js
    switch (expression) {
        case x:
            // execute case x code block
            break;
        case y:
            // execute case y code block
            break;
        default:
            // execute default code block
    }
    ```
18. What is the syntax for a ternary operator?
    * condition ? expression if true : expression if false
19. What is nesting?
    * Nesting is to write something inside of another item.
        ```js
        if (daylight) {
        if (before 12) {
            //It's morning;
            } else {
            // it's afternoon;
            }
        }
        ``` 
# JavaScript Developer Tools
## Knowledge Check
1. How do you open developer tools?
	- F12
	- Inside the menu of your browser 
	- Right-click on a webpage item and click inspect
2. How do you change screen size of a website using developer tools?
    * You utilize the 'Device Mode' within the developer tools. This lets you simulate the sizes of various devices to run on websites.
3. What is a breakpoint?
    * A breakpoint lets you inspect what your code is doing at a certain point of its execution. This lets you see what values are stores in which variables and more.
4. How do you set a breakpoint?
    * You click on the line number and it will set a flag there so that the debugger knows where to stop.
# Foundations Part 3
## Knowledge Check
1. What are functions useful for?
	* Functions allow us to do simple tasks by calling it and supplying arguments.
2. How do you invoke a function?
	```js
    function function_name(arg){
		}
	```	
3. What are anonymous functions?
	* They are functions without a name. Anonymous functions are usually used along with an event handler.
        ```js
        const myButton = document.querySelector('button');

        myButton.onclick = function() {
            alert('hello');
        }
        ```
4. What is function scope?
	* Function scope is the scope of the variables that are inside the function. Those variables cannot be accessed by anything outside of that function.
5. What are return values?
    * Return values are the values returned after calling the function.
6. What are arrow functions?
	* Arrow functions are function expressions with a simpler and concise syntax.
	* let func = (arg1, arg2, ..., argN) => expression
        ```js
        let sum = (a, b) => a + b;

        /* This arrow function is a shorter form of:

        let sum = function(a, b) {
            return a + b;
        };
        */
        ```
# Problem Solving
## Knowledge Check
1. What are the three stages in the problem solving process?
    * Understand the problem, plan, and divide & conquer.
2. Why is it important to clearly understand the problem first?
    * You may waste a lot of time doing an objective that doesn't pertain to the problem.
3. What can you do to help get a clearer understanding of the problem?
    * Rewrite the problem in your own words. 
4. What are some of the things you should do in the planning stage of the problem solving process?
    * Ask some of the following questions:
    * Does your program have a user interface? What will it look like? What functionality will the interface have? Sketch this out on paper.
    * What inputs will your program have? Will the user enter data or will you get input from somewhere else?
    * What’s the desired output?
    * Given your inputs, what are the steps necessary to return the desired output?
5. What is an algorithm?
    * An algorithm is a solution to problems that goes step-by-step.
6. What is pseudo code?
    * Rather than coding the problem, you can "code" the problem in natural language. Example:
        ```
        When the user inputs a number
        Initialize a counter variable and set its value to zero
        While counter is smaller than user inputted number increment the counter by one
        Print the value of the counter variable
        ```
7. What are the advantages of breaking a problem down and solving the smaller problems?
    * Solving the smaller problems will eventually add up together in solving the larger problem at hand.
# Understanding Errors
## Knowledge Check
1. What are three reasons why you may see a TypeError?
    * When an operand or argument passed to a function is incompatible with the type expected.
    * When attempting to change a value that cannot be changed.
    * When attempting to use a value in a manner that is prohibited.
2. What is the key difference between an error and a warning?
    * A warning simply signals to the user that a problem may occur. An error will completely stop the program when attempting to run.
3. What is one method you can use to resolve an error?
    * Completely read the error, it often lets you know which line in the code it occurred. Also use Google as there is often the case of another person running into the same problem as you, this could lead to finding a solution.

# Clean Code

## Knowledge Check
1. Why is it important to write clean code?
    * Having clean code will allow for anyone using it to have better understanding of how it works.
2. Name 5 clean code principles previously mentioned.
    * Use correct indentation
    * Write explanatory comments
    * Use correct naming standards for functions and variables
    * Avoid extremely large functions
    * Avoid having a large number of comments
3. What is the difference between good comments and bad comments?
    * Bad comments include those that are vague and do not pertain to the comment's purpose of better understanding the code. Good comments should be easy to understand and straight-to-the-point.

# Foundations Part 4
## Knowledge Check

1. What is an array?
    * An array is a variable that can hold a list of values.
    	```js 
    	const array_name = [item1, item2, ...];
    	// or
    	const array_name = new Array(item1, item2, ...);
    	```
2. What are arrays useful for?
    * Arrays are useful in that rather than having X amount of variables, each holding a different value, you can have an array of X length of all the different values under a single variable.
3. How do you access an array element?
    * You can access an array element using the element's index value.
    	```js
    	const cars = ["Saab", "Volvo", "BMW"];
    	let car = cars[0]; // returns Saab
    	```
4. How do you change an array element?
    * Similar to accessing the element, you can change it using the index value.
    	```js
    	const cars = ["Saab", "Volvo", "BMW"];
    	cars[0] = "Opel";
    	```
5. What are some useful array properties?
    * ```.length``` returns the number of elements within the array.
    * You can access the last array element b
6. What are some useful array methods?
    * ```Array.sort()``` sorts the array.
    * ```Array.forEach()``` loops through the array.
    * ```Array.push()``` adds an element to the end of the array.
    * ```Array.pop()``` removes the element at the end of the array.
7. What are loops useful for?
    * Loops are useful in helping the user iterate a task, using different variables, through lines of code multiple times.
8. What is the break statement?
    * The break statement will immediately terminate the current loop and resume at the next statement. 
9. What is the continue statement?
    * The continue statement will force the next iteration of the loop to take place.
10. What is the advantage of writing automated tests?
    * Through Test Driven Development (TTD), you want to first write a test that uses the function and supplies the expected output. This helps so that you don't have to write the code multiple times before being satisfied with the outputs.

# DOM Manipulation and Events
## Notes
1. DOM
    * Document Object Model
    * Tree-like representation of the contents of a webpage. The tree has nodes with different relationships depending on their arrangement inside the HTML document.
        ```html
            <div id="container">
                <div class="display"></div>
                <div class="controls"></div>
            </div>
        ```
    * The "display" class is a child of "container" whilst a sibling to "controls".
2. Selectors
    * You can use selectors to target the nodes you want to work with, through a combination of CSS-style selectors and relationship properties.
        ```html
            <div id="container">
                <div class="display"></div>
                <div class="controls"></div>
            </div>
        ```
    * For the above example, you can use the following selectors to refer to the "display" div:
        1. div.display
        2. .display
        3. #container > .display
        4. div#container > div.display
    * You can also use relational selectors (such as firstElementChild or lastElementChild) with special properties owned by the nodes.
        ```js
            const container = document.querySelector('#container');
            // select the #container div

            console.dir(container.firstElementChild);                      
            // select the first child of #container => .display

            const controls = document.querySelector('.controls');   
            // select the .controls div

            console.dir(controls.previousElementSibling);                  
            // selects the prior sibling => .display
        ```
3. DOM methods
    * When HTML is parsed by a web browser, it is converted to the DOM. Through this, nodes are objects and thus have many properties and methods attached to them. These properties and methods can be used to manipulate the webpage with JavaScript.
        1. Query Selectors
            * `element.querySelector(selector)` returns reference to the first match of selector
            * `element.querySelectorAll(selectors)` returns a “nodelist” (not an array but can be converted into one using Array.from() or the spread operator) containing references to all of the matches of the selectors
        2. Element Creation
            * `document.createElement(tagName, [options])` creates a new element of tag type tagName. [options] in this case means you can add some optional parameters to the function.
            ```js
                const div = document.createElement('div');
            ```
            * The above function is ONLY created in memory and NOT into DOM. You can manipulate the element (by adding styles, classes, etc.) before placing it on the page.
        3. Append Elements
            * `parentNode.appendChild(childNode)` appends childNode as the last child of parentNode
            * `parentNode.insertBefore(newNode, referenceNode)` inserts newNode into parentNode before referenceNode
        4. Remove Elements
            * `parentNode.removeChild(child)` removes child from parentNode on the DOM and returns reference to child
        5. Altering Elements
            * When you have a reference to an element, you can use that reference to alter the element’s own properties. This allows you to do many useful alterations, like adding/removing and altering attributes, changing classes, adding inline style information and more.
            ```js
                const div = document.createElement('div');
                // create a new div referenced in the variable 'div'
            ```
        6. Adding inline style
            ```js
                const div = document.createElement('div');
                // create a new div referenced in the variable 'div'

                div.style.color = 'blue';                                      
                // adds the indicated style rule

                div.style.cssText = 'color: blue; background: white';          
                // adds several style rules

                div.setAttribute('style', 'color: blue; background: white');    
                // adds several style rules
            ```
            * More information on inline styles [DOM Enlightenment: Getting, setting, & removing individual inline CSS properties](http://domenlightenment.com/#6.2)
            * If the CSS rule is in kebab-case (using dashes between words rather than spaces), you'll have to use camelcase or bracket notation instead of dot notation.
            ```js
                div.style.background-color // doesn't work - attempts to subtract color from div.style.background
                div.style.backgroundColor // accesses the divs background-color style
                div.style['background-color'] // also works
                div.style.cssText = "background-color: white" // ok in a string
            ```
        7. Editing Attributes
            ```js
                div.setAttribute('id', 'theDiv');                              
                // if id exists update it to 'theDiv' else create an id with value "theDiv"

                div.getAttribute('id');                                        
                // returns value of specified attribute, in this case "theDiv"

                div.removeAttribute('id');                                     
                // removes specified attribute
            ```
            * More information about available attributes [MDN: HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
        8. Working with classes
            ```js
                div.classList.add('new');                                      
                // adds class "new" to your new div

                div.classList.remove('new');                                   
                // remove "new" class from div

                div.classList.toggle('active');                                
                // if div doesn't have class "active" then add it. Or if it does, then remove it
            ```
            * It's often more standard and clean to toggle a CSS style over adding and removing inline CSS.
        9. Adding text content
            ```js
                div.textContent = 'Hello World!'                               
                // creates a text node containing "Hello World!" and inserts it in div
            ```
        10. Adding HTML content
            ```js
                div.innerHTML = '<span>Hello World!</span>';                   
                // renders the html inside div
            ```
        11. Complete Example
            ```html
                <!-- your html file: -->
                <body>
                    <h1>
                        THE TITLE OF YOUR WEBPAGE
                    </h1>
                    <div id="container"></div>
                </body>
            ```
            ```js
                // your javascript file
                const container = document.querySelector('#container');

                const content = document.createElement('div');
                content.classList.add('content');
                content.textContent = 'This is the glorious text-content!';

                container.appendChild(content);
            ```
            * In the JS file, we get a reference to the `container` div that already exists in the HTML file. Then a new div is created and stored as `content`. We add a class and some text to '`content` and append that to the reference `container`.
            * After the JS code is run, the DOM tree will look like this:
            ```html
                <!-- The DOM -->
                <body>
                    <h1>
                        THE TITLE OF YOUR WEBPAGE
                    </h1>
                    <div id="container">
                        <div class="content">
                        This is the glorious text-content!
                        </div>
                    </div>
                </body>
            ```
            * REMINDER: That the JS only alters the DOM and not the HTML. The HTML file will look the same but the JS changes what the browser renders.
            * If you write your JS code at the top of your file, many DOM methods will not work bcause the JS code is being run before the nodes are created in the DOM. To fix this, you either write the JS code at the bottom of the HTML file or you link the JS file inside the `<head>` tag.
4. Events
    * JavaScript can be used to make out webpage listen and react to events (actions that occur on the webpage like mouse-clicks or keypresses).
    * There are three ways to do this:
        1. Attach functions' attributes directly on the HTML elements. This can clutter the HTML with JavaScript and you can only have 1 "onclick" event per element.
            ```html
                <button onclick="alert('Hello World')">Click Me</button>
            ```
        2. Set the "on_event_" property on the DOM object in the JavaScript. Though cleaner, you can still only have 1 "onclick" property.
            ```html
                <!-- the html file -->
                <button id="btn">Click Me</button>
            ```
            ```js
                // the JavaScript file
                const btn = document.querySelector('#btn');
                btn.onclick = () => alert("Hello World");
            ```
        3. Attach event listeners to the nodes in the JavaScript.
            ```html
                <!-- the html file -->
                <button id="btn">Click Me Too</button>
            ```
            ```js
                // the JavaScript file
                const btn = document.querySelector('#btn');
                btn.addEventListener('click', () => {
                    alert("Hello World");
                });
            ```
        4. All 3 of these methods can be used with named functions.
            ```html
                <!-- the html file -->
                <!-- METHOD 1 -->
                <button onclick="alertFunction()">CLICK ME BABY</button>
            ```
            ```js
                function alertFunction() {
                alert("YAY! YOU DID IT!");
                }

                // METHOD 2
                btn.onclick = alertFunction;

                // METHOD 3
                btn.addEventListener('click', alertFunction);
            ```
    * You can also attach listeners to a group of nodes using  `querySelectorAll('selector')` and then iterating though the list.
        ```html
            <div id="container">
                <button id="1">Click Me</button>
                <button id="2">Click Me</button>
                <button id="3">Click Me</button>
            </div>
        ```
        ```js
            // buttons is a node list. It looks and acts much like an array.
            const buttons = document.querySelectorAll('button');

            // we use the .forEach method to iterate through each button
            buttons.forEach((button) => {

            // and for each one we add a 'click' listener
            button.addEventListener('click', () => {
                alert(button.id);
            });
            });
        ```
    * NOTE: You may get an error of `Uncaught TypeError: [] is null` inside the JS file. This can be fixed by adding `defer` to the `script` tag inside the HTML file as such: `<script src="script.js" defer></script>`
    * There are many more useful events (click, dblclick, keypress, keydown, keyup). 
    * List of DOM events and their description can be found [HERE](https://www.w3schools.com/jsref/dom_obj_event.asp)
## Knowledge Check
1. What is the DOM?
    * The DOM (or Document Object Model) is a tree-like representation of the contents of a webpage - a tree of “nodes” with different relationships depending on how they’re arranged in the HTML document.
2. How do you target the nodes you want to work with?
    * Selectors or Relational Selectors
3. How do you create an element in the DOM?
    * `document.createElement(tagName, [options])`
    * Ex) `const div = document.createElement('div');`
4. How do you add an element to the DOM?
    * `parentNode.appendChild(childNode)` appends childNode as the last child of parentNode
    * `parentNode.insertBefore(newNode, referenceNode)` inserts newNode into parentNode before referenceNode
5. How do you remove an element from the DOM?
    * `parentNode.removeChild(child)` removes child from parentNode on the DOM and returns reference to child
6. How can you alter an element in the DOM?
    * You create a reference to an element and use that reference to alter the element through changing attributes, classes and other inline style information.
7. When adding text to a DOM element, should you use textContent or innerHTML? Why?
    * textContent/innerText because innerHTML information is rendered as HTML, which could be used as a way for HTML injection.
8. Where should you include your JavaScript tag in your HTML file when working with DOM nodes?
    * You should either have link a JavaScript file into the `<head>` tag or include the JavaScript code at the bottom of the HTML file.
    * This is to avoid any potential errors of JavaScript being run and affecting the DOM before the entire HTML code has been run.
9. How do “events” and “listeners” work?
    * Events are actions that occur on the webpage (mouse-clicks or keypresses) and listeners can "listen" for these events and react to them. 
10. What are three ways to use events in your code?
    * You can attach the functions' attributes directly on the HTML element
    * You can set the "on_event_" property on the DOM object in your JavaScript
    * You can attach event listeners to the nodes in your JavaScript
11. Why are event listeners the preferred way to handle events?
    * Event listeners are able to scale with complex programs through iteration.
12. What are the benefits of using named functions in your listeners?
    * It allows for code to be much cleaner and can be reused in multiple places.
13. How do you attach listeners to groups of nodes?
    * You get a nodelist of all the items matching the selector using `querySelectorAll('selector')`
    * Then you iterate through the nodelist using the `.forEach` method.
14. What is the difference between the return values of querySelector and querySelectorAll?
    * `querySelector` returns reference to the first match of the selector
    * `querySelectorAll` returns a "nodelist" containing references to all of the matches of the selectors.
15. What does a “nodelist” contain?
    * It contains references to the nodes inside the nodelist. However, while it looks and somewhat acts like an array, it is not an array due to missing several array methods. This can be fixed by converting the nodelist into an array.
16. Explain the difference between “capture” and “bubbling”.
    * Information from [quirksmode.org](https://www.quirksmode.org/js/events_order.html)
    * When you use event capturing, the event handler of element1 fires first, the event handler of element2 fires last.
    ```
                       | |
        ---------------| |-----------------
        | element1     | |                |
        |   -----------| |-----------     |
        |   |element2  \ /          |     |
        |   -------------------------     |
        |        Event CAPTURING          |
        -----------------------------------
    ```
    * When you use event bubbling, the event handler of element2 fires first, the event handler of element1 fires last.
    ```
                       / \
        ---------------| |-----------------
        | element1     | |                |
        |   -----------| |-----------     |
        |   |element2  | |          |     |
        |   -------------------------     |
        |        Event BUBBLING           |
        -----------------------------------
    ```
# Fundamentals Part 5
## Notes
1. Objects
    * Note: Some code fragments taken from [Javascript.info](https://javascript.info/object)
    * Objects are used to store keyed collections of various data.
        * Objects can be created with two different syntaxes:
            1. Using figure brackets { } with an optional list of properties. A property is a pair of keys and values (key: value). The key is a string, also referred to as a 'property name', and value, which can be anything.
                ```js
                // This is the "object literal" syntax
                let user = {     // an object
                    name: "John",  // by key "name" store value "John"
                    age: 30,       // by key "age" store value 30
                    "likes birds": true, // multiword property name must be quoted 
                                         // (note that you can end the last property with & without a comma)
                };
                ```
            2. Using the object constructor
                ```js
                // This is the "object constructor" syntax
                let user = new Object(); 
                ```
        * An object's property values can be accessed through dot notation.
            ```js
            alert( user.name ); // John
            alert( user.age ); // 30
            ```
        * We can also add and remove values as such:
            ```js
            user.isAdmin = true; // Adds the key 'isAdmin' with the boolean value true
            delete user.age; // Removes both the key and value for the user's age
            ```
        * In order to access multiword properties, dot notation will not suffice. As such, we need to use square bracket notation.
            ```js
            // this would give a syntax error
            user.likes birds = true

            // this works
            user["likes birds"] = true // set

            alert(user["likes birds"]); // get

            delete user["likes birds"]; // delete
            ```
        * When utilizing square brackets in an object literal, when creating an object, that's called computed propeties.
            ```js
            let fruit = prompt("Which fruit to buy?", "apple");

            let bag = {
                [fruit]: 5, // the name of the property is taken from the variable fruit
            };

            alert( bag.apple ); // 5 if fruit="apple"
            ```js
        * In real code, programmers often use the same names for both property names and values. This can be simplified utilizing the property value shorthand.
            * The following code has both 'name: name' & 'age: age'.
                ```js
                function makeUser(name, age) {
                    return {
                        name: name,
                        age: age,
                        // ...other properties
                    };
                }

                let user = makeUser("John", 30);
                alert(user.name); // John
                ```
            * The above code simplified using the shorthand for property values.
                ```js
                function makeUser(name, age) {
                    return {
                        name, // same as name: name
                        age,  // same as age: age
                        // ...
                    };
                }
                ```
        * While a variable cannot have the same name as one of the language-reserved words ('for', 'let', 'return', etc.), an object *can* have those as names. 
            ```js
            // these properties are all right
            let obj = {
                for: 1,
                let: 2,
                return: 3
            };

            alert( obj.for + obj.let + obj.return );  // 6
            ```
        * Without such limitations, both strings and symbols can be used as names. Other types, such as integers, are converted into strings as well. There is one limitation: an object with property named ```__proto__``` cannot be set to a non-object value.
            ```js
            let obj = {};
            obj.__proto__ = 5; // assign a number
            alert(obj.__proto__); // [object Object] - the value is an object, didn't work as intended
            ```
        * We can access any property, even if it doesn't exist using the "in" operator
            ```js
            // syntax: "key" in object

            let user = { name: "John", age: 30 };

            alert( "age" in user ); // true, user.age exists
            alert( "blabla" in user ); // false, user.blabla doesn't exist
            ```
        * The special "for..in" loop alows us to iterate through all the keys of an object.
            * Syntax
                ```js
                    for (key in object) {
                        // executes the body for each key among object properties
                    }
                ```
            * Example
                ```js
                let user = {
                    name: "John",
                    age: 30,
                    isAdmin: true
                };

                for (let key in user){
                    // keys
                    alert( key ); // Iteration order: name, age, isAdmin

                    // values for keys
                    alert( user[key] ) // Iteration order: John, 30, true
                }
                ```
        * Objects are ordered in special order. Integer properties (which are strings that can be converted to-and-from an integer without changing, i.e. "49" can be both an integer and string) are sorted from low to high, while other properties will appear in creation order.
            * Integer properties
                ```js
                let codes = {
                "49": "Germany",
                "41": "Switzerland",
                "44": "Great Britain",
                "1": "USA"
                };

                // integer properties are listed in the numerical order
                for (let code in codes) {
                alert(code); //Order: 1, 41, 44, 49
                }
                ```
            * Non-integer properties
                ```js
                let user = {
                name: "John",
                surname: "Smith"
                };
                user.age = 25; // add one more

                // non-integer properties are listed in the creation order
                for (let prop in user) {
                alert( prop ); // name, surname, age
                }
                ```
            * How to get around integer properties: add "+" before each code to turn them into non-integers.
                ```js
                let codes = {
                "+49": "Germany",
                "+41": "Switzerland",
                "+44": "Great Britain",
                "+1": "USA"
                };

                // non-integer properties are listed in the creation order
                for (let code in codes) {
                alert(code); //Order: 49, 41, 44, 1
                }
                ```
2. Quick Objects Summary from Javascript.info
    * Objects are associative arrays with several special features.
    * They store properties (key-value pairs), where:
        * Property keys must be strings or symbols (usually strings).
        * Values can be of any type.
    * To access a property, we can use:
        * The dot notation: ```obj.property```.
        * Square brackets notation ```obj["property"]```. Square brackets allow taking the key from a variable, like ```obj[varWithKey]```.
    * Additional operators:
        * To delete a property: ```delete obj.prop```.
        * To check if a property with the given key exists: ```"key" in obj```.
        * To iterate over an object: ```for (let key in obj)``` loop.
    * What we’ve studied in this chapter is called a “plain object”, or just ```Object```.
    * There are many other kinds of objects in JavaScript:
        * ```Array``` to store ordered data collections,
        * ```Date``` to store the information about the date and time,
        * ```Error``` to store the information about an error.
## Knowledge Check
1. What is the difference between objects and arrays?
    * Objects are used to store properties in key-value value pairs. Arrays, a form of an object, store data in an ordered collection and can be accessed via indices.
2. How do you access object properties?
    * We can use the dot notation (```obj.property```) or the square bracket notation (```obj["property"]```).
3. What is ```Array.prototype.map()``` useful for?
    * Some code taken from [Wes Bos' video](https://www.youtube.com/watch?v=HB1ZC7czKRs)
    * The map() function takes in an array, handles an operation on the array, and returns a new array of the **same length**.
        ```js
        const inventors = [
            { first: "Albert", last: "Einstein", year: 1879, passed: 1955},
            { first: "Isaac", last: "Newton", year: 1643, passed: 1727},
            { first: "Galileo", last: "Galilei", year: 1564, passed: 1642},
            { first: "Marie", last: "Curie", year: 1934, passed: 1934}
        ]

        const fullNames = inventors.map(inventor => inventor.first + ' ' + inventor.last);
        console.log(fullNames) // ['Albert Einstein', 'Isaac Newton', 'Galileo Galilei', 'Marie Curie']
        ```
4. What is ```Array.prototype.reduce()``` useful for?
    * The reduce() function allows the user to execute a 'reducer' callback function on each element of the array. The resulting value, is then utilized in the next iteration's function. The final result will be a single value.
        ```js
        const array1 = [1, 2, 3, 4];

        // 0 + 1 + 2 + 3 + 4
        const initialValue = 0;
        const sumWithInitial = array1.reduce(
        (accumulator, currentValue) => accumulator + currentValue, initialValue
        );

        console.log(sumWithInitial);
        // Expected output: 10
        ```
        ```js
        const totalYears = inventors.reduce((total, inventor) => {
            return total + (inventor.passed - inventor.year)
        }, 0);

        console.log(totalYears) // 523
        ```