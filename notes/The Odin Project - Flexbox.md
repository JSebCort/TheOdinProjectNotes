# Introduction to Flexbox
## Knowledge Check
1. What’s the difference between a flex container and a flex item?
    * A flex item is an element that lives inside a flex container.
2. How do you create a flex item?
    * To create a container, use 'display:flex'. Otherwise, flex items are simply elements inside a flex container.
# Growing and Shrinking
## Notes
1. Default values of the 'flex' property are flex-grow: 0, flex-shrink: 1, flex-basis: 0%
2. flex-grow : This value is used as the item's 'growth factor'.
    * This means that every div inside the container will grow the same amount. If another div has a flex-grow value of 2, it'll be 2x the size of others.
3. flex-shrink : This value is used as the item's 'shrink factor'. 
    * This means that the item will shrink if the size of all flex items is larger than the flex container.
4. flex-basis : This value sets the initial main size of a flex item. 
    * If a flex item's flex-basis is set to 200px, it's initial size will be 200x and will then shrink if needed.
## Knowledge Check
1. What are the 3 values defined in the shorthand flex property (e.g. flex: 1 1 auto)?
    * Using 'flex: 1 1 auto'
        * 1 : flex-grow 
        * 1 : flex-shrink
        * auto : flex-basis
# Axes
## Notes
1. A flexbox can work either horizontally (row) or vertically (column), with the default direction being horizonal.
2. If the flex-direction is column, the flex-basis refers to height instead of width.
## Knowledge Check
1. How do you make flex items arrange themselves vertically instead of horizontally?
    * flex-direction: column
2. In a column flex-container, what does flex-basis refer to?
    * width
3. In a row flex-container, what does flex-basis refer to?
    * height
4. Why do the previous two questions have different answers?
    * If a flex-container's direction is a column, then the height is based on the content of the flex item rather than the width of the flex item's box.
# Alignment
## Notes
1. 'justify-content' 
    * Aligns items across the main axis (x-axis / horizontally)	
    * flex-start: Lines the items up at the start of the edge of the container
    * flex-end: Lines the items up at the end of the container
    * center: Lines the items up at the center of the container
    * space-between: Takes all the container's space and shares it evenly between the items, leaving an equal amount of space between the items.
    * space-around: Gives equal amount of space between the left and right of each item, though the end items will have half-size space.
    * space-evenly: To not have half-size space next to the end items, use space-evenly.
2. 'align-items'
	* Aligns items across the cross axis (y-axis / vertically)
	* flex-start : Makes the items line up at the start of the flex container (top right)
	* flex-end : Aligns the items to the end (bottom left)
	* center : Aligns the items in the center
	* stretch : The default value; The flex items switch to the height of the flex container.
3. flex-direction has 4 values:
	* row (main axis runs along in the inline direction \ cros axis runs down the columns)
	* row-reverse
	* column (main axis runs from the top of the page to the bottom \ cross axis runs along the rows)
	* column-reverse
4. 'flex-wrap'
	* Value of 'wrap' allows for items to wrap to the next line if they are too large to display in one line.
	* 'nowrap' (default value) will cause items to shrink to fit the container.
5. 'flex-flow'
	* Combination of flex-direction and flex-flow
	* Structed as 'flex-flow: flex-direction flex-flow'
	    * Ex) 'flex-flow: row wrap;'
6. More information:
	* https://css-tricks.com/snippets/css/a-guide-to-flexbox/
	* https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox
	* https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container
	* https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Typical_Use_Cases_of_Flexbox
## Knowledge Check
1. What is the difference between justify-content and align-items?
    * 'justify-content' aligns on the main axis, 'align-items' aligns on the cross axis.
2. How do you use flexbox to completely center a div inside a flex container?
    * 'justify-content: center'
    * 'align-items: center'
3. What’s the difference between justify-content: space-between and justify-content: space-around?
    * 'space-between' doesn't give space to the right of left of the end items while 'space-around' gives half-space.
