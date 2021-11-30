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