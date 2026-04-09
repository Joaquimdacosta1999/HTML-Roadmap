# HTML Images

Images can improve the design and the appearance of a web page.

### Example
``` html
<img src="pic_trulli.jpg" alt="Italian Trulli">
```
### Example
```html
<img src="img_girl.jpg" alt="Girl in a jacket">
```

### Example
```html 
<img src="img_chania.jpg" alt="Flowers in Chania">
```

## HTML Images Syntax

The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

- The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

- The `<img>` tag has two required attributes:

---

- `src` : Specifies the path to the image
- `alt` : Specifies an alternate text for the image

## Syntax

```html
<img src="url" alt="alternatetext">
```

## The src Attribute

The required `src` attribute specifies the path (URL) to the image.

<b>Note</b>: When a web page loads, it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken `link` icon. The broken `link` icon and the alt text are shown if the browser cannot find the image.

### Example
``` html
<img src="img_chania.jpg" alt="Flowers in Chania">
```
## The alt Attribute

The required `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the `src` attribute, or if the user uses a screen reader).

The value of the alt attribute should describe the image:

### Example
```htm
<img src="img_chania.jpg" alt="Flowers in Chania">
```

If a browser cannot find an image, it will display the value of the alt attribute:


### Example
```html
<img src="wrongname.gif" alt="Flowers in Chania">
```

<b>Tip</b>: A screen reader is a software program that reads the HTML code, and allows the user to "listen" to the content. Screen readers are useful for people who are visually impaired or learning disabled.

## Image `Size` - `Width` and `Height`

You can use the style attribute to specify the width and height of an image.

### Example
```html
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">
```
Alternatively, you can use the `width` and `height` attributes:

### Example
```html
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```

The `width` and `height` attributes always define the `width` and `height` of the image in pixels.

<b>Note</b>: Always specify the width and height of an image. If width and height are not specified, the web page might flicker while the image loads.


## Width and Height, or Style?

The `width`, `height`, and `style` attributes are all valid in HTML.

However, we suggest using the style attribute. It prevents styles sheets from changing the size of images:

### Example
```html
<!DOCTYPE html>
<html>
<head>
<style>
/* This style sets the width of all images to 100%: */
img {
  width: 100%;
}
</style>
</head>
<body>

<h2>Width/Height Attributes or Style?</h2>

<p>The first image uses the width attribute (set to 128 pixels), but the style in the head section overrides it, and sets the width to 100%.</p>

<img src="html5.gif" alt="HTML5 Icon" width="128" height="128">

<p>The second image uses the style attribute to set the width to 128 pixels, this will not be overridden by the style in the head section:</p>

<img src="html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">

</body>
</html>
```
<p>
<img src="/HTML Fundamental/Source/img link.png">
</p>

## Images in Another Folder

If you have your images in a sub-folder, you must include the folder name in the `src` attribute:

### Example
``` html
<img src="/images/html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">
```

## Images on Another Server/Website

Some web sites point to an image on another server.

To point to an image on another server, you must specify an absolute (full) URL in the src attribute:

### Example
``` html
<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">
```

<b>Notes on external images</b>: External images might be under copyright. If you do not get permission to use it, you may be in violation of copyright laws. In addition, you cannot control external images; they can suddenly be removed or changed.

## Animated Images

HTML allows animated GIFs:

### Example
``` htm
<img src="programming.gif" alt="Computer Man" style="width:48px;height:48px;">
```

## Image as a Link

To use an image as a `link`, put the `<img>` tag inside the `<a>` tag:

### Example
``` htm
<!DOCTYPE html>
<html>
<body>

<h2>Image as a Link</h2>

<p>The image is a link. You can click on it.</p>

<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>

</body>
</html>
```

## Image Floating

Use the CSS float property to let the image float to the right or to the left of a text:

### Example
``` html
<!DOCTYPE html>
<html>
<body>

<h2>Floating Images</h2>
<p><strong>Float the image to the right:</strong></p>

<p>
<img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
A paragraph with a floating image. A paragraph with a floating image. A paragraph with a floating image.
</p>

<p><strong>Float the image to the left:</strong></p>
<p>
<img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
A paragraph with a floating image. A paragraph with a floating image. A paragraph with a floating image.  
</p>

</body>
</html>
```
---

## HTML Image Maps

With HTML image maps, you can create clickable areas on an image.

## Image Maps

The HTML `<map>` tag defines an image map. An image map is an image with clickable areas. The areas are defined with one or more `<area>` tags.

### Example

Here is the HTML source code for the image map above:

``` html 
<!DOCTYPE html>
<html>
<body>

<h2>Image Maps</h2>
<p>Click on the computer, the phone, or the cup of coffee to go to a new page and read more about the topic:</p>

<img src="workplace.jpg" alt="Workplace" usemap="#workmap" width="400" height="379">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Cup of coffee" href="coffee.htm">
</map>

</body>
</html>
```
The idea behind an image map is that you should be able to perform different actions depending on where in the image you click.

To create an image map you need an image, and some HTML code that describes the clickable areas.

## The Image

The image is inserted using the `<img>` tag. The only difference from other images is that you must add a usemap attribute:

<img src="workplace.jpg" alt="Workplace" usemap="#workmap">

The usemap value starts with a hash tag # followed by the name of the image map, and is used to create a relationship between the image and the image map.

## Create Image Map

Then, add a `<map>` element.

The `<map>` element is used to create an image map, and is linked to the image by using the required name attribute:

`<map name="workmap">`

The name attribute must have the same value as the `<img>`'s usemap attribute .


## The Areas

Then, add the clickable areas.

A clickable area is defined using an `<area>` element.

## Shape

You must define the shape of the clickable area, and you can choose one of these values:

- <b>rect</b> - defines a rectangular region
- <b>circle</b> - defines a circular region
- <b>poly</b> - defines a polygonal region
- <b>default</b> - defines the entire region

You must also define some coordinates to be able to place the clickable area onto the image. 

<b>Shape="rect"</b>

The coordinates for `shape="rect"` come in pairs, one for the x-axis and one for the y-axis.

So, the coordinates 34,44 is located 34 pixels from the left margin and 44 pixels from the top:
<p><img src="/HTML Fundamental/Source/34.png"></p>

### Workplace

The coordinates 270,350 is located 270 pixels from the left margin and 350 pixels from the top:
<p>
<img src="/HTML Fundamental/Source/270,350.png">
</p>

### Workplace

Now we have enough data to create a clickable rectangular area:

### Example
``` html
<!DOCTYPE html>
<html>
<body>

<h2>Image Maps</h2>
<p>Click on the cup of coffee to go to a new page and read more about the topic:</p>

<img src="workplace.jpg" alt="Workplace" usemap="#workmap" width="400" height="379">

<map name="workmap">
  <area shape="circle" coords="337,300,44" alt="Cup of coffee" href="coffee.htm">
</map>

</body>
</html>
```
<p><img src="/HTML Fundamental/Source/coffee.htm.png"></p>

This is the area that becomes clickable and will send the user to the page "computer.htm":

Workplace
Shape="circle"
To add a circle area, first locate the coordinates of the center of the circle:

337,300

Workplace
Then specify the radius of the circle:

44 pixels

Workplace
Now you have enough data to create a clickable circular area:

Example
<area shape="circle" coords="337, 300, 44" href="coffee.htm">
This is the area that becomes clickable and will send the user to the page "coffee.htm":

Workplace
Shape="poly"
The shape="poly" contains several coordinate points, which creates a shape formed with straight lines (a polygon).

This can be used to create any shape.

Like maybe a croissant shape!

How can we make the croissant in the image below become a clickable link?

French Food
We have to find the x and y coordinates for all edges of the croissant:

French Food
The coordinates come in pairs, one for the x-axis and one for the y-axis:

Example
<area shape="poly" coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147" href="croissant.htm">
This is the area that becomes clickable and will send the user to the page "croissant.htm":

French Food
Image Map and JavaScript
A clickable area can also trigger a JavaScript function.

Add a click event to the <area> element to execute a JavaScript function:

Example
Here, we use the onclick attribute to execute a JavaScript function when the area is clicked:

<map name="workmap">
  <area shape="circle" coords="337,300,44" href="coffee.htm" onclick="myFunction()">
</map>

<script>
function myFunction() {
  alert("You clicked the coffee cup!");
}
</script>
Chapter Summary
Use the HTML <map> element to define an image map
Use the HTML <area> element to define the clickable areas in the image map
Use the HTML usemap attribute of the <img> element to point to an image map