# CSS Notes 

## 1.0 Introduction 

CSS is a styling language that determines the way in which HTML elements are displayed. The function of CSS can be discribed by placing a container around HTML elements and assigning properties to each individual container is styled. An example of how CSS works in conjunction with HTML is displayed in the following diagram: 

*picture goes where*

The syntax of CSS is distinguished by two parts: the selector, and the declaration. 

- Selector: Refers to which HTML elements should be styled. 

- Declaration: How the elements should be styled. Each declaration ends with a semi colon (;).  

```CSS 

p {
	font-family: Times, serif;
}

```

### 1.1 How to use CSS 

CSS can be applied to HTML in two following ways. 

1. CSS can be applied in the form of a CSS file. This can be used by the corresponding HTML file by using the `<link>` tag in the `<head>` element block. 

- <link>: Attributes of link 

	- href : The file pathway or url of the CSS file. 

	- type: Type of document that is being linked `text/CSS` for CSS 

	- rel: Relationship of the file to HTML page. Should be `stylesheet`

2. Can be directly applied to the HTML file by using the `style` tage in the `<head>` element block. 

## #1.2 Selector types: 

- ` * {} ` - Applies to all elements 

-  `h1, h2, h3 {}` - Applies to the target elements 

- `.note {}` -  Applies the element with class "note"

- `#introduction {}` - Applies to elements with the ID Introduction

- `li>a {}` - Applies to the element which is the direct child of li named a. 

- `p a {}` - Applies to the target a descendant of p. Nested*

- `h1+p` - Applies to the element that comes after h1.

- `h1-p`- Applies to all the p sibilings of h1. 

CSS styling rules take precendence in terms of most recent rules and specificity. Rules are also inherited from parent elements and can be overwritten. 

## 2.0 Color 

The color can be changed in CSS using the following values: 

- `rgb/rgba (int, int, int, [0,1]) ` - rgb values (+optional opaquity value for rbga)  

- `#ffffff` - hex values 

- predefined color names 

- `hsl/hsla (int, %, %, [0,1])` - Hue, Saturation, Lightness (&transparency). 

Properties of Color include the following: 

- color - Color of text

- background-color

- opacity

## 3.0 Text 

Typefaces in CSS are described into 5 categories: 

- Serif: Extra detail at the end of characters (ex. Georgia, Times) 

- San Serif: No extra detail, cleaner design and straighter (ex. Arial, Verdana) 

- Monospace: Each letter has the same width (ex. Courier) 

- Cursive: Looks like handwritten cursive and letters link up (ex. Comic Sans) 

- Fantasy: Decorative fonts, condensed (ex. Impact) 

*Usually CSS declarations for font-family will have more than one font-family given that all browsers aren't guarenteed to have availble font type. Usually these generic typeface descriptions are declared at the end to tell the browser to at least use a certain font with the same typeface. (ex. font-family: "Courier New", Monospace;) 

Font sizes can be described in 3 ways in CSS: 

- Pixels - The size of pixels a letter should take. Almost similar to pt system in most document software. 

- Percentage - Percentage in comparison to the default font size of browsers (16px). 

- Em - Size is relative to font given by the parent element. 

`@font-face` is a special kind of selector that specifies that if a user's browser does not have a certain font, they can download it from the following path. You need to specify both the font-family, src, and the format for the declaration. There can be multiple src for different formats needed to support different browsers. 

Text properties: 

- font-family: The name of the font type. 

- font-size: How large should the font be.

- font-weight: Whether it is normal or bold. 

- font-style: Whether it's normal, italicized, or oblique. 

- text-transform: Whether text is uppercase, lowercase, or capitalized. 

- text-decoration: whether text has none, underline, overline, or blink decoration.  

- line-height: The height of a letter. (leading). 

- letter-spacing, word-spacing: self explanatory. 

- text-align: Whether the text is aligned left, right, center, justify (every line except the last line should take up the full width of the container). 

- vertical-align: Allows vertical alignment for inline elements (NOT TEXT) like images or table cells. (example values: baseline, top, middle, bottom). 

- text-indent: Self-explanatory. 

- text-shadow(size, size, (optional size), color) : CSS3 property that allows you to place a shadow on text. It request the following values (length of shadown left or right, length of shadow top or bottom, optionally the amount of blur applied, color of shadow). 

### 3.1 Psuedo-elements: 

Psuedo-elements are applied at the end of selectors and specify specific versions of the element 

Versions on text: 

- :first-letter - Applies to the first letter of the element 

- :first-line -Applies to the first line of the element 

- :link - Only styles the text if the link associated has not been visited. 

- :visited - Only styles the text if the link associated has been visited.

- :hover - Only styles if the mouse if on the element 

- :active - Only styles when the element is pressed.

- :focus - Only styles when the element is ready to be interacted with. (example tabing on certain elements or forms.  

### 3.2 Attribute Selectors

CSS also always selectors to apply to elements with specific attributes to them. Here's a list of such attribute selectors:

 - [] - Matches a specific attribute. (ex. `p[class]`)

- [=] - Matches a specific attribute with a value (ex. `p[class = "dog"]`)

- [~=] - Matches a specific attribute with a space separate list of values (ex. `p[class~="dog"] for <p class ="cat dog"> )

- [^=] - Matches a specific attribute with a value beginning with a substring (ex. `p[attr^="d"]);

- [*=] - Matches a specific attribute with a value with a substring (ex. `p[attr*="do"]);

- [$=] - Matches a specific attribute with a value ending with a substring (ex. `p[attr$="g"]);

## 4.0 Boxes 

Every CSS container has the following basic formatting properties: 

- Border - How the border of a container is styled, whether it has lines and how do those lines look. 

- Margin - How far the container must be from other containers. 

- Padding - How far the content inside the container must be away from the border. 

Properties of Boxes:

*Note: All properties that request a size uses either pixels, percentage, or em, as a form of measurement. Any additional form will be noted. 

- width, height - Specifies the width and height of the box.

- min-width, max-width - specifies the minimum and maximum width of a box. 

- min-height, max-height - Specifies the minimum and maximum height of a box 

- overflow - Describes the style when content within the box exceeds the size allowed. Has the values scroll and hidden. 

- border: A short-hand way to describe all the properties of border. And requests them in the following order (border: border-width, border-style, border-color). 

	- border-width: Specifies the width of border. Requests the basic form of measurements or predefined sizes thin, medium, thick.  You can control individual sizes of the border by specifying the area of the border (*ex. border-top-width*). Also a shortcut method would be to assign four values to border width. (border-width: top, right, bottom, left).  

	- border-style: Specifies the style of the border. Has the following styles: solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none. Can control individual styles using the same technique as border-width. (*ex. border-left-style*).  Also a shortcut method would be to assign four values to border style. *(border-style: top, right, bottom, left)*.  

	- border-color: Specifies using the standard color. Takes the standard measurements for color. Can control individual styles using the same technique as border-width. *(ex. border-left-color).*  Also a shortcut method would be to assign four values to border color. *(border-color: top, right, bottom, left)*.  

- padding: Specifies much space should be between the border and the content.   Can control individual styles  *(ex. padding-left)*.  Also a shortcut method would be to assign four values to padding *(ex. padding: top, right, bottom, left*). 

- margin: Controls the gap between boxes. Can control individual styles  *(ex. margin-left)*.  Also a shortcut method would be to assign four values to margin *(ex. margin: top, right, bottom, left)*. 

-display: Turns inline elements to block elements, and vice-versa. Values are *inline, block, inline-block, none*. 

-visibility: Allows you to hide boxes from user. Values hidden, visible. 

CSS3 properties: 

- border-image: Applies image to the border of the box and requests for three values. 

	1. Where the image is (url) 

	2. Where to slice the image 

	3. How to display image. stretch: strech the image, repeat: repeat the image. round: repeat and scale the image to fit. 

- box-shadow: Creates shadow around the box. Asks for the following value (Horizontal Offset, Vertical Offset, (Blur Distance-Can be for both/optional), Spread of Shadow). Inset can be used before to denote when you want an inner shadow. 

- border-radius: Border corners are smoothen out. Can control each corner individually (ex. border-top-right-radius). Can be shorthanded and manipulate the x and y radius of each corner (ex. border-radius 1em 2em 1em 2em/ 2em 4em 2em 4em --- horizontal/vertical). 

## 5.0 Datasets 

### 5.1 Lists 

Properties of list: 

- list-style-type: Controls the shape and style of the bullet point: 

	-unordered list: none, disc, circle, square. 

	-ordered list: decimal, decimal-leading-zero, lower-alpha, upper-alpha, lower-roman, upper-roman. 

- list-style-image: specifies an image to act as a bullet point. Needs a (url).

- list-style-position: Specifies whether the bullet point should be part of the content or outside the content-box (indented). Values requested are inside, or outside. 

- list-style: shorthand for type/image, position. 

### 5.2 Tables

Properties already elaborated on which can be applied to tables: 

-  width

- padding, 

- text-transform 

- letter-spacing, font size 

- border-top, border-botom 

- text-align 

- background color 

- :hover 

Tips for styling tables:  

- Give cells padding 

- Distinguish headings

- Shade alternative rows 

- Align numerals 

New properties: 

- empty-cells - specifies whether or not borders should be shown for empty cells. Has values show, hide, inherit 

- border-spacing - Specifies how much should the borders between each cell should be spaced if space is needed. 

- border-collapse - Overwrites `border-spacing` when table cells should have no space between them. Has values separate and collapse. 

### 5.3 Forms 

#### Styling text input 

Tips: Use font-size, color, background color, border, border-radius, :focus, :hover, background-image. 

#### Styling submit buttons

Tips: color, text-shadow, border-bottom, background-color. 

#### Styling fieldsets and legends 

Tips: color, background-color, width, border, border-radius, padding. 

- `cursor` - Cursor property allows you to control the style and type of mouse that is displayed. Ex( auto, crosshair, default, pointer, move, text, wait, help, url(image.gif)). 

## 6.0 Layout 

### 6.1 Positioning elements

- `position:` - Property that determines the position of an HTML element relative to a certain object on the webpage.
	- normal(*static*)- The default positionin of HTML elements where each block element flows from top to bottom and is separated by white space. 

	- relative - Indicates the position of an HTML element relative to where it was suppose to be if it was normal. The offset is defined by the properties(*top* or *bottom*, *left* or *right*). 

	- absolute - Taken out of normal flow and does not affect the positioning of the rest of the elements. It appears in relation to the containing element.  
	The offsets are defined the same as relative.

	- fixed - Same as absolute but in relation to the webpage. 

- `z-index` - 

- `float` - Takes elements in normal flow and stacks them on the left or right of a page. 

- `clear` - Tells the web page that not elements should be placed on the left and right-hand side of a box. 
Values are - *left, right, both, none*. 

\*Tips: You can use width, margin, float to create multiple columns of content. 

\*Pages are often designed around having a width of *960-1000 pixels* and the top page being a height of *570-600 pixels*.

### 6.2 Fixed Vs Liquid Layout 
A fixed layout uses px as a form of measurement. The size of the content are static and are often used to design sites with the main audience being PC users. 

Meanwhile, liquid layout uses % and *em* as a form of measurement in order to scale content to variety of devices with different screen resolutions. 

### 6.3 960.GS framework 
Provides (framework for HTML sites)[https://960.gs/]. 
 

## 7.0 Images 

- background: Shortcut for the following properties. Can miss any of the values

	- background-color: Covered 
	- background-image: Takes in url. 
	- background-repeat: Values are *repeat* horizontally and vertically), *repeat-x, repeat-y, no-repeat*. 
	- background-attachment: *fixed*(background image stays in place), *scroll*(moves as you scroll). 
	- background-position: 9 different coordinates as horizontal-vertical section *(ex. center-top)* Can also take coordinates. 

Gradients can also be added to images. 

## Miscellaneous

### Comments 

Comments in CSS are written in between the `/* Comment goes here */`

### Links 

Links are specified as `url()` in declaration. 

### Multiple CSS file 

You can use `@import{}` to import different CSS files. or `<link>` them in terms of precedence in the HTML file. 

