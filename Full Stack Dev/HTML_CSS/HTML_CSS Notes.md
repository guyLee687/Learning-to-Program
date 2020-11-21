
# HTML Notes

## 1.0 Introduction

HTML is a markup language that uses "*markup*" labels and character texts in order to organize information on a webpage in a form of 
structure. Standard text is conveyed in between HTML tags, each with their own name, attributes, and values, which are denoted inside 
a bracket `</>`. HMTL elements will often start with and end with a bracket creating a **code block**, which either describe the structure or semantics of information. 

An instance of such is the following: 

```HTML
    <p>
        <!--Stuff inside a code--> 
        ...
    </p>
``` 

* **Note**: Tags can have *attributes* within them that further specify the kind of information being markedup with the tag. **Attributes** have a *name* that specifies the property, and the *value*- that the state of the attribute. (Ex. `<p lang="en-us">`)

### 1.1 Format 

An HTML document usually follow the take on the form as follows: 

```HTML
    <!DOCTYPE html>
    <html>
        <head> </head>
        <body> </body>
    </html> 
```
 - `<DOCTYPE html>` species the type of HTML version the file is being used. Given that there has been multiple version of HTML that has been developed. It's may be necessary depending on type of browser this webpage is being sent too. The `html` value species we are using the latest version **HTML5**. 

## 2.0 Text 

The way in which text is affected by HTML works in two parts. *Block elements* an *inline elements*. 
**Block elements**
: HTML elements that enclose standard text and/or other HTML elements. They create a block a text that will add a newline space before and after the content within its brackets if there is no styling involved. 

**Inline elements** 
: HTML elements that only act within a line of text. There is no newline being consumed once it is specified. 

### 2.1 Block Elements 

Examples of block elements involve, headings, paragraphs, and other structural based markup. 
- ` h1, ..., h6 ` - Headers 
- ` p ` - Paragraphs  
- `div` - Acts a container for block elements kinda like sections on a newspaper. 

### 2.2 Inline elements 

Examples of Inline elements involve semantic based markup usually that involve things that emphasize the importances or purpose of words: 
- `b, i, sup, sub` - bold text, italicized text, superscript, subscript. 
- `<br />, <hr />` - line break and horizontal line 
- `<ins>, <del>, <s>(being phased out)` - Insert, delete, strikethrough
- `<cite>, <address>, <dfn>` - Cite, address, define. 
- `<strong>, <em>` - Same as bold and italicized but they allow for some software to place more meaning to them (ex. web reader for visual-impaire). 
- `<abbr>` - Denotes an abbrivation. Has *title* attribute which expands on the abbreviation. When hovered upon, it will show what it means. 


## 3.0 Data Presentation

### 3.1 List 
#### Unordered List 
Unordered lists are presented as the following: 
```HTML
    <ul>
        <li></li>
        ...
    </ul>
```

#### Ordered List 
Ordered lists are presented as the same as Unordered list but by replacing `<ul>` with `<ol>`

#### Definition List 
Definition lists are presentedd as the following: 
```HTML
    <dl>
        <dt></dt> <!--Definition Term-->
        <dd></dd> <!--Definition Defined-->
        ...
    </dl>
```
Both `dt` and `dd` can be used more than once and does not need to be in a one-to-one pair. 

### 3.2 Tables
Tables are enclosed with the following tags `<table> </table>`. It has several different attributes and variations of such. 

> Attributes 
- spacing 
- borders
- background color 

Most attributes are being discontinued and rely on *CSS* in order to style tables. 

To specify what is in a table you use the following tags. 
- `<th scope = "">` - table header where scope refers to what the scope of the header is for.
- `<tr>` - table row.
- `<td col/rowspan = "">` - table data where *colspan* or *rowspan* refers to how much the data extends further than an individual cell. 

Tables can also be broken up by a 
- *thead*
- *tbody*
- *tfoot* 

for styling with CSS. 

## 4.0 Forms 

## 5.0 Links

## 6.0 Media Input 
### 6.1 Images
Images are placed with 

## Miscellenous 

### Commenting 
-  Commenting in HTML is done through the use of a bracket enclosed with an exclamation market a two dots. 
    `<!--This is a comment-->`