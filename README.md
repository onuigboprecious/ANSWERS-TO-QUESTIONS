# ANSWERS-TO-QUESTIONS
answers to few questions on HTML and CSS!
#ANSWER TO N0-1
A rectangle box is wrapped around every HTML element. The box model is used to determine the height and width of the rectangular box. The CSS Box consists of Width and height (or in the absence of that, default values and the content inside), padding, borders, margin.
Properties-  Content:  Actual Content of the box where the text or image is placed.
             Padding: Area surrounding the content (Space between the border and content).
             Border: Area surrounding the padding.
             Margin: Area surrounding the border.

#ANSWER TO N0-2
advantages of css.
Bandwidth - Used effectively, the style sheets will be stored in the browser cache and they can be used on multiple pages, without having to download again.

Easy to maintain - CSS, built effectively can be used to change the look and feel complete by making small changes. To make a global change, simply change the style, and all elements in all the web pages will be updated automatically.

Separation of content from presentation - CSS provides a way to present the same content in multiple presentation formats in mobile or desktop or laptop.


#ANSWER TO N0-3
limitations:
Browser Compatibility: Some style selectors are supported and some are not. We have to determine which style is supported or not using the @support selector).
Cross Browser issue: Some selectors behave differently in a different browser).
There is no parent selector: Currently, Using CSS, you can’t select a parent tag.


#ANSWER TO N0-4
There are different ways to include a CSS in a webpage, 

a - External Style Sheet: An external file linked to your HTML document: Using link tag, we can link the style sheet to the HTML page.
<link rel="stylesheet" type="text/css" href="mystyles.css" />

b - Embed CSS with a style tag: A set of CSS styles included within your HTML page.
<style type="text/css">
/*Add style rules here*/
</style>
Add your CSS rules between the opening and closing style tags and write your CSS exactly the same way as you do in stand-alone stylesheet files.

c - Add inline styles to HTML elements(CSS rules applied directly within an HTML tag.): Style can be added directly to the HTML element using a style tag.
<h2 style="color:red; background:black">Inline Style</h2>

d - Import a stylesheet file (An external file imported into another CSS file): Another way to add CSS is by using the @import rule. This is to add a new CSS file within CSS itself.
@import "path/to/style.css";

#ANSWER TO N0-5

A CSS selector is the part of a CSS ruleset that actually selects the content you want to style. Different types of selectors are listed below.

a. Universal Selector: The universal selector works like a wildcard character, selecting all elements on a page. In the given example, the provided styles will get applied to all the elements on the page.
* {
  color: "green";
  font-size: 20px;
  line-height: 25px;
}

b. Element Type Selector: This selector matches one or more HTML elements of the same name. In the given example, the provided styles will get applied to all the ul elements on the page.
ul {
  line-style: none;
  border: solid 1px #ccc;
}

c. ID Selector: This selector matches any HTML element that has an ID attribute with the same value as that of the selector. In the given example, the provided styles will get applied to all the elements having ID as a container on the page.
#container {
  width: 960px;
  margin: 0 auto;
}
<div id="container"></div>

d. Class Selector: The class selector also matches all elements on the page that have their class attribute set to the same value as the class.  In the given example, the provided styles will get applied to all the elements having ID as the box on the page.
.box {
  padding: 10px;
  margin: 10px;
  width: 240px;
}
<div class="box"></div>

e. Descendant Combinator: The descendant selector or, more accurately, the descendant combinator lets you combine two or more selectors so you can be more specific in your selection method.
#container .box {
	float: left;
	padding-bottom: 15px;
} 
<div id="container">
	<div class="box"></div>
	<div class="box-2"></div>
</div>
<div class=”box”></div>
This declaration block will apply to all elements that have a class of box that is inside an element with an ID of the container. It’s worth noting that the .box element doesn’t have to be an immediate child: there could be another element wrapping .box, and the styles would still apply.

f. Child Combinator: A selector that uses the child combinator is similar to a selector that uses a descendant combinator, except it only targets immediate child elements.
#container> .box {
	float: left;
	padding-bottom: 15px;
}
<div id="container">
	<div class="box"></div>
	
	<div>
		<div class="box"></div>
	</div>
</div>
The selector will match all elements that have a class of box and that are immediate children of the #container element. That means, unlike the descendant combinator, there can’t be another element wrapping .box it has to be a direct child element.

g. General Sibling Combinator: A selector that uses a general sibling combinator to match elements based on sibling relationships. The selected elements are beside each other in the HTML.
h2 ~ p {
	margin-bottom: 20px;
}
<h2>Title</h2>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<div class=”box”>
	<p>Paragraph example.</p>
</div>
In this example, all paragraph elements (<p>) will be styled with the specified rules, but only if they are siblings of <h2> elements. There could be other elements in between the <h2> and <p>, and the styles would still apply.

h. Adjacent Sibling Combinator: A selector that uses the adjacent sibling combinator uses the plus symbol (+), and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling.
p + p {
	text-indent: 1.Sem;
	margin-bottom: 0;
}
<h2>Title</h2>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<p>Paragraph example.</p>

<div class=”box”>
	<p>Paragraph example.</p>
	<p>Paragraph example.</p>
</div>
The above example will apply the specified styles only to paragraph elements that immediately follow other paragraph elements. This means the first paragraph element on a page would not receive these styles. Also, if another element appeared between two paragraphs, the second paragraph of the two wouldn’t have the styles applied.

i. Attribute Selector: The attribute selector targets elements based on the presence and/or value of HTML attributes, and is declared using square brackets.
   input [type=”text”] {
	 background-color: #444;
	 width: 200px;
   }

  <input type="text">

#ANSWER TO N0-6
A CSS Preprocessor is a tool used to extend the basic functionality of default vanilla CSS through its own scripting language. It helps us to use complex logical syntax like – variables, functions, mixins, code nesting, and inheritance to name a few, supercharging your vanilla CSS.

SASS: Sass is the acronym for “Syntactically Awesome Style Sheets”. SASS can be written in two different syntaxes using SASS or SCSS

SASS vs SCSS

SASS is based on indentation and SCSS(Sassy CSS) is not.
SASS uses .sass extension while SCSS uses .scss extension.
SASS doesn’t use curly brackets or semicolons. SCSS uses it, just like the CSS.
SASS Syntax

$font-color: #fff 
$bg-color: #00f

#box
	color: $font-color
	background: $bg-color
SCSS Syntax

$font-color: #fff;
$bg-color: #00f;

#box{
	color: $font-color;
	background: $bg-color;
}
  
LESS: LESS is an acronym for “Leaner Stylesheets”. LESS is easy to add to any javascript projects by using NPM or less.js file. It uses the extension .less.

LESS syntax is the same as the SCSS with some exceptions. LESS uses @ to define the variables.

@font-color: #fff;
@bg-color: #00f

#box{
	color: @font-color;
	background: @bg-color;
}
Stylus: Stylus offers a great deal of flexibility in writing syntax, supports native CSS as well as allows omission of brackets, colons, and semicolons. It doesn’t use @ or $ for defining variables.

/* STYLUS SYNTAX WRITTEN LIKE NATIVE CSS */
font-color= #fff;
bg-color = #00f;

#box {
	color: font-color;
	background: bg-color;
}

/* OR */

/* STYLUS SYNTAX WITHOUT CURLY BRACES */
font-color= #fff;
bg-color = #00f;

#box
	color: font-color;
	background: bg-color;

#ANSWER TO N0-7
It’s a CSS unit used to measure the height and width in percentage with respect to the viewport. It is used mainly in responsive design techniques. The measure VH is equal to 1/100 of the height of the viewport. If the height of the browser is 1000px, 1vh is equal to 10px. Similarly, if the width is 1000px, then 1 vw is equal to 10px.

#ANSWER TO N0-8
Reset CSS: CSS resets aim to remove all built-in browser styling. For example margins, paddings, font-sizes of all elements are reset to be the same. 

Normalize CSS: Normalize CSS aims to make built-in browser styling consistent across browsers. It also corrects bugs for common browser dependencies.

#ANSWER TO N0-9
a. Block Element: The block elements always start on a new line. They will also take space for an entire row or width. List of block elements are <div>, <p>.

b. Inline Elements: Inline elements don't start on a new line, they appear on the same line as the content and tags beside them. Some examples of inline elements are <a>, <span> , <strong>, and <img> tags. 

c. Inline Block Elements: Inline-block elements are similar to inline elements, except they can have padding and margins and set height and width values.

#ANSWER TO N0-10
It’s most important to test a website in different browsers when you’re first designing it, or when making major changes. However, it’s also important to repeat these tests periodically, since browsers go through a lot of updates and changes.

#ANSWER TO N0-11
Pseudo-elements allows us to create items that do not normally exist in the document tree, for example ::after.

::before
::after
::first-letter
::first-line
::selection
In the below example, the color will appear only on the first line of the paragraph.

p: :first-line {
	color: #ffOOOO;
	font-variant: small-caps;
}
Pseudo-classes select regular elements but under certain conditions like when the user is hovering over the link.

:link
:visited
:hover
:active
:focus
Example of the pseudo-class, In the below example, the color applies to the anchor tag when it’s hovered.

/* mouse over link */
a:hover {
	color: #FFOOFF;
}

#ANSWER TO N0-12
There are different ways to specify units in CSS like px, em, pt, percentage (%). px(Pixel) gives fine-grained control and maintains alignment because 1 px or multiple of 1 px is guaranteed to look sharp. px is not cascade. em maintains relative size. you can have responsive fonts. Em, will cascade 1em is equal to the current font-size of the element or the browser default. If u sent font-size to 16px then 1em = 16px. The common practice is to set default body font-size to 62.5% (equal to 10px).

pt(point) are traditionally used in print. 1pt = 1/72 inch and it is a fixed-size unit.

%(percentage) sets font-size relative to the font size of the body. Hence, you have to set the font-size of the body to a reasonable size

#ANSWER TO N0-13
No, it doesn’t affect the inline elements. Inline elements flow with the contents of the page.

#ANSWER TO N0-14
We can use the font-family property for achieving this. The font-family property is used for specifying what font needs to be applied on the targetted DOM element. It can hold several font names as part of “fallback” mechanism in case the browser does not support the fonts. For example, we can use:

 p {
  font-family: "Times New Roman", Times, serif;
}
In the above piece of code, we are applying font-family property to the paragraph element.

It tells the browser to look for “Times New Roman” font and apply it.
If the “Times New Roman” font is not installed or supported, then it asks the browser to use Times font.
If both “Times New Roman” and Times are not supported, then it asks the browser to use any supported generic font belonging to serif.
If you do not want the font-face of the paragraph element to be Times New Roman/Times/serif font, and you want to use the Arial/Helvetica/sans-serif font, then we can just update the CSS property of paragraph element as:

 p {
  font-family: Arial, Helvetica, sans-serif;
}  

#ANSWER TO N0-15
differences between adaptive design and responsive design:
adaptive design- When a website developed using adaptive design is opened on the desktop browser, first the available space is detected and then the layout with most                    appropriate sizes are picked and used for the display of contents. Resizing of browser window has no affect on the design.
  
responsive design-When a website developed using responsive design is opened on a desktop browser and when we try to resize the browser window, the content of the                       website is dynamically and optimally rearranged to accomodate the window.

#ANSWER TO N0-16
The order of matching selectors goes from right to left of the selector expression. The elements in the DOM are filtered by browsers based on the key selectors and are then traversed up to the parent elements for determining the matches. The speed of determining the elements depends on the length of the chain of selectors. Consider an example:

 p span{ 
    color: black;
}
Here, the browser first finds all span elements in the DOM and then it traverses to each of its parent elements to check if they are the paragraph p elements.
Once the browser finds all matching span tags having paragraph elements as parent and applies the color of black to the content, the matching process is stopped.

#ANSWER TO N0-17
content-box: is the default value box-sizing property. The height and the width properties consist only of the content by excluding the border and padding.
while; The border-box property includes the content, padding and border in the height and width properties.

#ANSWER TO N0-18
Opacity refers to the degree to which the content is transparent or opaque. We can use the property named opacity which takes the values ranging from 0 to 1. 0 specifies that the element is completely transparent where 1 means that the element is completely opaque. We can use the opacity property as follows:
 .body { 
    opacity: 0.6;
}

#ANSWER TO N0-19
  The float property is used for positioning the HTML elements horizontally either towards the left or right of the container. For instance,

 float-demo {
     float: right; 
}
  or 
 float-demo {
       float:left;
  }
   
#ANSWER TO N0-20
z-index is used for specifying the vertical stacking of the overlapping elements that occur at the time of its positioning. It specifies the vertical stack order of the elements positioned that helps to define how the display of elements should happen in cases of overlapping.

The default value of this property is 0 and can be either positive or negative. Apart from 0, the values of the z-index can be:

a. Auto: The stack order will be set equal to the parent.
b. Number: The number can be positive or negative. It defines the stack order.
c. Initial: The default value of 0 is set to the property.
d. Inherit: The properties are inherited from the parent.
The elements having a lesser value of z-index is stacked lower than the ones with a higher z-index.

#ANSWER TO N0-21
  a. div, p: This selector implies selecting all div elements and all p elements.
  b. div p: This selector tells to select all p elements that are inside div elements.
  c. div ~ p : This selector tells to select all p elements that have div elements preceeded anywhere
  d. div + p : This selector says to select all p elements placed immediately after the div element. 
  e. div > p : This selector says to select all p elements which has div as an immediate parent.
  
#ANSWER TO NO-22
The properties of flexbox are as follows:
 a. flex-direction: This property helps in defining the direction the container should stack the items targetted for flex. The values of this property can be 
  i.row: Stacks items horizontally from left to right in the flex container.
  ii.column: Stacks items vertically from top to bottom in the flex container.
  iii.row-reverse: Stacks items horizontally from right to left in the flex container.
  iv column-reverse: Stacks items vertically from bottom to top in the flex container.
  
b. flex-wrap: This property specifies of the flex items should be wrapped or not. Possible values are:
  i. wrap: The flex items would be wrapped if needed.
  ii. nowrap: This is the default value that says the items won’t be wrapped.
  iii. wrap-reverse: This specifies that the items will be wrapped if needed but in reverse order.
  
c. flex-flow: This property is used for setting both flex-direction and flex-wrap properties in one statement.
  
d. justify-content: Used for aligning the flex items. Possible values are:
  i. center: It means that all the flex items are present at the center of the container.
  ii. flex-start: This value states that the items are aligned at the start of the container. This is the default value.
  iii. flex-end: This value ensures the items are aligned at the end of the container.
  iv. space-around: This value displays the items having space between, before, around the items.
  v. space-between: This value displays items with spaces between the lines.
  
e. align-items: This is used for aligning flex items.
  
f. align-content: This is used for aligning the flex lines
  
#ANSWER TO NO-23
Cascading” refers to the process of going through the style declarations and defining weight or importance to the styling rules that help the browser to select what rules have to be applied in times of conflict.  This is done by using the "!important" word along side it's value. !important ensures that the property has the maximum weight in presence of other conflicting properties.
 
  #ANSWER TO NO-24
a. Absolute: To place an element exactly where you want to place it. absolute position is actually set relative to the element's parent. if no parent is available then    the relative place to the page itself (it will default all the way back up to the element).
  
b. Relative: "Relative to itself". Setting position: relative; on an element and no other positioning attributes, it will no effect on its positioning. It allows the      use of z-index on the element and it limits the scope of absolutely positioned child elements. Any child element will be absolutely positioned within that block.
  
c. Fixed: The element is positioned relative to the viewport or the browser window itself. viewport doesn't change if you scroll and hence the fixed element will stay    right in the same position. 
  
d. Static: Static default for every single page element. The only reason you would ever set an element to position: static is to forcefully remove some positioning        that got applied to an element outside of your control.
  
e. Sticky: Sticky positioning is a hybrid of relative and fixed positioning. The element is treated as relative positioned until it crosses a specified threshold, at      which point it is treated as fixed positioned
  
#ANSWER TO NO-25
Reflow occurs when:

  a. Insert, remove or update an element in the DOM.
  b. Modify content on the page, e.g. the text in an input box.
  c. Move a DOM element.
  d. Animate a DOM element.
  e. Take measurements of an element such as offsetHeight or getComputedStyle.
  f. Change a CSS style
  
#ANSWER TO NO-26
  There are the following CSS properties use to hide an element.

   a. Absolute position
   b.Color
   c. Clip-path
   d. Display
   e. filter
   f. Measurements
   g. Opacity
   h. Transform
   i. Visibility
  
  #ANSWER TO NO-27
  The :root selector allows you to target the highest-level “parent” element in the DOM, or document tree.
  It is defined in the CSS Selectors Level 3 specification.
  
  #ANSWER TO NO-28
  CSS Grid Layout is a two-dimensional system, meaning it can handle both columns and rows. Grid layout is intended for larger-scale layouts which aren’t linear in       design. While
  Flexbox is largely a one-dimensional system (either in a column or a row). Flexbox layout is most appropriate to the components of an application.
  
  #ANSWER TO NO-29
  The style is having the "!important" will have the highest precedence and it overrides the cascaded property.
  
  #ANSWER TO NO-30
  Margin are used to create space around an elements.
  while; paddling are used for generating the space around the element’s content and inside any known border.
  ####################################################-----THE END----------#########################################################
