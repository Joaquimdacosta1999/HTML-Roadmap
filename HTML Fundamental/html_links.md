# HTML Links

Links are found in nearly all web pages. Links allow users to click their way from page to page.

## HTML Links - Hyperlinks

HTML links are hyperlinks.

You can click on a link and jump to another document.

When you move the mouse over a link, the mouse arrow will turn into a little hand.

<b>Note</b>: A link does not have to be text. A link can be an image or any other HTML element!

## HTML Links - Syntax

The HTML `<a>` tag defines a hyperlink. It has the following syntax:

``` html 
<a href="url">link text</a>
```

The most important attribute of the `<a>` element is the href attribute, which indicates the link's destination.

The link text is the part that will be visible to the reader.

Clicking on the link text, will send the reader to the specified URL address.

### Example

This example shows how to create a link to W3Schools.com:

``` html 
<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
```

By default, links will appear as follows in all browsers:

- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red

## HTML Links - The target Attribute

By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.

The `target` attribute specifies where to open the linked document.

The `target` attribute can have one of the following values:

- `_self` - Default. Opens the document in the same window/tab as it was clicked
- `_blank` - Opens the document in a new window or tab
- `_parent` - Opens the document in the parent frame
- `_top` - Opens the document in the full body of the window

### Example

Use `target="_blank"` to open the linked document in a new browser window or tab:
``` html
<a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a>
```

## Absolute URLs vs. Relative URLs

Both examples above are using an absolute URL (a full web address) in the `href` attribute.

A local link (a link to a page within the same website) is specified with a relative URL (without the "https://www" part):

### Example
``` html 
<h2>Absolute URLs</h2>
<p><a href="https://www.w3.org/">W3C</a></p>
<p><a href="https://www.google.com/">Google</a></p>

<h2>Relative URLs</h2>
<p><a href="html_images.asp">HTML Images</a></p>
<p><a href="/css/default.asp">CSS Tutorial</a></p
```

## HTML Links - Use an Image as a Link

To use an image as a link, just put the `<img>` tag inside the `<a>` tag:

## Example
<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>

<p>
<img src="/HTML Fundamental/Source/i.png">
</p>

## Link to an Email Address

Use `mailto`: inside the href attribute to create a link that opens the user's email program (to let them send a new email):

### Example
``` html
<a href="mailto:someone@example.com">Send email</a>
```

## Button as a Link

To use an HTML button as a link, you have to add some JavaScript code.

JavaScript allows you to specify what happens at certain events, such as a click of a button:

### Example
``` html
<!DOCTYPE html>
<html>
<body>

<h2>Button as a Links</h2>

<p>Click the button to go to the HTML tutorial.</p>

<button onclick="document.location='default.asp'">HTML Tutorial</button>

</body>
</html>
```
<p>
<img src="/HTML Fundamental/Source/JavaScript.png">
</p>

## Link Titles

The `title` attribute specifies extra information about an element. The information is most often shown as a tooltip text when the mouse moves over the element.

### Example
``` html
<a href="https://www.w3schools.com/html/" title="Go to W3Schools HTML section">Visit our HTML Tutorial</a>
```

## More on Absolute URLs and Relative URLs

### Example

Use a full URL to link to a web page: 
``` html 
<a href="https://www.w3schools.com/html/default.asp">HTML tutorial</a>
```

### Example

Link to a page located in the html folder on the current web site: 
``` html
<a href="/html/default.asp">HTML tutorial</a>
```

### Example

Link to a page located in the same folder as the current page: 
``` html
<a href="default.asp">HTML tutorial</a>
```
## Chapter Summary
- Use the `<a>` element to define a link
- Use the `href` attribute to define the `link` address
- Use the `target` attribute to define where to open the `linked` document
- Use the `<img>` element (inside `<a>`) to use an image as a `link`
- Use the `mailto`: scheme inside the href attribute to create a `link` that opens the user's email program

---

## HTML `Links` - Different Colors

An HTML `link` is displayed in a different color depending on whether it has been visited, is unvisited, or is active.

HTML Link Colors

By default, a `link` will appear like this (in all browsers):

- An unvisited `link` is underlined and blue
- A visited `link` is underlined and purple
- An active `link` is underlined and red

You can change the link state colors, by using CSS:

Example
Here, an unvisited link will be green with no underline. A visited link will be pink with no underline. An active link will be yellow and underlined. In addition, when mousing over a link (a:hover) it will become red and underlined:

``` css
<style>
a:link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}

a:visited {
  color: pink;
  background-color: transparent;
  text-decoration: none;
}

a:hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}

a:active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}
</style>
```

## Link Buttons

A link can also be styled as a button, by using CSS:

### Example

``` html
<!DOCTYPE html>
<html>
<head>
<style>
a:link, a:visited {
  background-color: #f44336;
  color: white;
  padding: 15px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
</style>
</head>
<body>

<h2>Link Button</h2>
<p>A link styled as a button:</p>
<a href="default.asp" target="_blank">This is a link</a>

</body>
</html>
```
<p>
<img src="/HTML Fundamental/html_links.md">
</p>

--- 

## HTML Links - Create Bookmarks

HTML links can be used to create bookmarks, so that readers can jump to specific parts of a web page.

## Create a Bookmark in HTML

Bookmarks can be useful if a web page is very long.

To create a bookmark - first create the bookmark, then add a link to it.

When the link is clicked, the page will scroll down or up to the location with the bookmark.


### Example

First, use the `id` attribute to create a bookmark:

``` html
<h2 id="C4">Chapter 4</h2>
``` 

Then, add a `link` to the bookmark ("Jump to Chapter 4"), from within the same page:

### Example

``` html
<!DOCTYPE html>
<html>
<body>

<p><a href="#C4">Jump to Chapter 4</a></p>
<p><a href="#C10">Jump to Chapter 10</a></p>

<h2>Chapter 1</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 2</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 3</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C4">Chapter 4</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 5</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 6</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 7</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 8</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 9</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C10">Chapter 10</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 11</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 12</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 13</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 14</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 15</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 16</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 17</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 18</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 19</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 20</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 21</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 22</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 23</h2>
<p>This chapter explains ba bla bla</p>

</body>
</html>
```

You can also add a link to a bookmark on another page:
``` html
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```

## Chapter Summary

- Use the id attribute `(id="value")` to define bookmarks in a page
- Use the href attribute `(href="#value")` to link to the bookmark