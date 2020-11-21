
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
The form (`<form id="" action="" method="">`) element is responsible for getting input from the user and sending that data to the path expressed by the *action* attribute. All form elements can also have a *id* attribute in order to distinguish itself from other elements and is often used in scripts. The *method* attribute is responsible for specifying the type of HTTP response the the form is sent to the *action* path (**GET*** for small data, and **POST** for larger data like files). 

Forms also have different form controls which specify the type of data and constraints to user input. 

### 4.1 Form controls
#### Input (<Input>)
Types: 
- text: Single line text with *name*, *size*, and *maxlength* attributes. 
- password: Same as text but hides the password. 
- textarea: Multiline text with *col* and *rol* attributes. 
- radio: Radio buttons with *name*, *value*, *checked* as attributes. 
- checkbox: Same as radio type except you can select and deselect multiple
- file: Allows user to upload file. *name* attribute. * **method** attribute must be set to **POST**
- submit: Submit button. *name* attribute - names the input type. *Value* - Defines the text on the submit button. 
- image: You can replace the submit button with an image. The attributes as the same for *submit* but replaces *value* with the attributes of image. 
- hidden: A hidden form control that the user has no control over. It has a *name* and *value* attribute that can be preset. A use could be to denote the page in which the user submitted the form if the form is shared across the domain. 

HTML5 Input Types: 
- date 
- email
- url 
- search - *placeholder* attribute for opaque lettering in search bar.


#### Select (<Select>)
A selection box.
Attributes: *name*, *size* - size of select box, *multiple* - specifies whether multiple options can be choosen from select box. 
Options from the select box are denoted with the `<option>` tag which has the following attributes. 
- *value*, *selected* - The option that is preselected with the page is loaded.  

#### Button (<Button>)
Takes the place of input type *submit* but can combine images and text inside of it. 

#### Label (<Label>)
Labels group together form controls with text in order to expand the clickable area for visually impaired users, and also helps with webreaders when parsing form controls. 
Attributes: *for* - Can take the form control *id* and encapsulate the form control with the label text. 

### Fieldset(<fieldset>)
Fieldset is simply used to group together multiple form controls. The header of the fieldset can be denoted with the tag `<legend>`.

* **Note**: Form validation can be added to textboxs by adding the *required* attribute. 
## 5.0 Links
Links are referenced through using the `<a>` tag. They have the following attributes. 
- *href* - where you place the link. It can be a *relative* or an *absolute* path. 
- *target* - If a new page is openned with the link (using macro "_blank")

* **Note**: You can add a `mailto:` term in front a link for the value of *href* in order to specify to the user's browser to open the user's email software. 
* **Note2**: You can add an *id* to headers and have links reference them on the same page by adding a `#` before the id in the link path. 

## 6.0 Media Input 
### 6.1 Images
Images are placed with `<img>` tag. It has the following attributes. 
- *src* - the location of the image in the webpage folder. 
- *alt* - Alternative text to display if the image can't be seen. Quotations can be ommitted if rules are not strict to denote insignificant images.
- *title* - Additional information about image. Browsers typically show this when users hover over the image. 
- *height*
- *width*
- *align* - Being phased out. 

### 6.2 Videos
Videos need a script to embed a video player and the media needs to be converted to a format applicable to the browser type. 
Uses `<video>` tag. Multiple videos can be referred using `<source>` tag. Audio is similar to video by using `<audio>` tag. 

A script that can be used to embed video players is *SWFObject* which can be found by Google's publicly available APIs. 

## Miscellenous 

### Commenting 
-  Commenting in HTML is done through the use of a bracket enclosed with an exclamation market a two dots. 
    `<!--This is a comment-->`

### Meta 
Descriptions of the webpage (metainformation)
Follows the form of: 
```HTML
    <meta name="" OR http-equiv=""
          content="">
```
#### Name types:  
- Description: 155 characters max description used by search engine. 
- Keywords: Significant words describing your website. 
- robots: whether or how the search engine includes your webpages. 

#### http-equiv types: 
- author: The author of the webpage. 
- pragma: no-cache or caching
- expires: when cache expires