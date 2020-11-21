
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
- `emp `

## Miscellenous 

### Commenting 
-  Commenting in HTML is done through the use of a bracket enclosed with an exclamation market a two dots. 
    `<!--This is a comment-->`