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

<img src="img_chania.jpg" alt="Flowers in Chania">

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
