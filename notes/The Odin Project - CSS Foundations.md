# CSS Foundations
## Knowledge Check
1. What are the main differences between external, internal, and inline CSS?
	* External has rules written in an external CSS file.
	* Internal has rules written inside the HTML file, within the head tags, using the style tag.
	* Inline has rules written within the opening tag of the element.
2. What is the syntax for class and ID selectors?
	* Class uses .
	* ID uses #
3. How would you apply a single rule to two different selectors?
    * You can list the selectors separated by commas before the rule.
4. Given an element that has an id of title and a class of primary, how would you use both attributes for a single rule?
    * .primary, #title
5. What does the descendant combinator do?
    * A descendant combinator allows for a rule to only apply to the element that matches the last selector of the rule.
	    * Ex) .ancestor .contents would only apply to an element whose parent is of class 'ancestor' and whose own class is 'contents'.
6. Between a rule that uses one class selector and a rule that uses three type selectors, which rule has the higher specificity?
    * The rule that has one class selector has higher specificity as it is more specific.
# Inspecting HTML and CSS
## Knowledge Check
1. How do you select a specific element on your page with your browser’s developer tools?
    * Mouse over the element, right-click and select "Inspect Element".
2. What does a strikethrough in a CSS element mean in your browser’s developer tools?
    * It means that while the style was used, it was overridden and a more specific selector's style was applied.
3. How do you change CSS in real time on specific elements of a web page with your browser’s developer tools?
    * After selecting an element inside the developer tools, their styles are shown next to the HTML code. These styles can be edited and shown in real time.
# The Box Model
## Knowledge Check
1. What does the box-sizing CSS property do?
    * Rather than the box's size being a sum of height or width, padding, and border, the size will now be the size that was specified in the css style.
2. Would you use margin or padding to create more space between 2 elements?
    * Margin; Padding only increased the space between the element's contents and the box's border.
3. Would you use margin or padding to create more space between the contents of an element and its border?
    * Padding
# Block and Inline
## Knowledge Check
1. What is the difference between a block element and an inline element?
    * Block elements create a 'block' for its element and essentially create a stack of elements. Inline elements do not start on a new line.
2. What is the difference between an inline element and an inline-block element?
    * inline-block elements act like inline elements but have the capability of their padding and margin to be edited.
3. Is an h1 block or inline?
    * block
4. Is span block or inline?
    * inline
5. Is button block or inline?
    * inline
6. Is div block or inline?
    * block