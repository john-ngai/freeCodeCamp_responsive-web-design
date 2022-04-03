# Section 1 - Basic HTML & HTML 5

[Responsive Web Design](https://www.freecodecamp.org/learn/responsive-web-design/) by freeCodeCamp.

# Say Hello to HTML Elements

Most HTML elements have an opening tag and a closing tag:

Opening tags look like this:

```html
<h1>
```

Closing tags look like this:

```html
</h1>
```

# Headline with the h2 Element

* `h1` elements are often used for main headings, while `h2` elements are generally used for subheadings.
  * There are also `h3`, `h4`, `h5`, and `h6` elements to indicate different levels of subheadings.

# Inform with the Paragraph Element

`p` elements are the preferred element for paragraph text on websites.

**Note:** As a convention, all HTML tags are written in lowercase, for example `<p></p>` and not `<P></P>`.

# Fill in the Blank with Placeholder Text

Web developers will commonly use the phrase, `lorem ipsum`, as placeholder text.

# Comment out HTML

Comments in HTML start with `<!--` and end with a `-->`.

# Introduction to HTML5 Elements

* HTML5 introduces more descriptive HTML tags.
  * These include `main`, `header`, `footer`, `nav`, `video`, `article`, `section` and others.
  * These tags give a descriptive structure to your HTML, make your HTML easier to read, and help with Search Engine Optimization (SEO) and accessibility.
    * For example, the `main` HTML5 tag helps search engines and other developers find the main content of your page.

```html
<main>
  <h1>Hello World!</h1>
  <p>Hello paragraph!</p>
</main>
```

**Note:** Many of the new HTML5 tags and their benefits are covered in the Applied Accessibility section.

# Add Images to Your Website

* You can add images to your website by using the `img` element, and point to a specific image's URL using the `src` attribute.
  * Note that `img` elements are **self-closing**.
* All `img` elements **must** also have an `alt` attribute.
  * The text inside an `alt` attribute is used for screen readers to improve accessibility and is displayed if the image fails to load.
  * **Note:** If the image is purely decorative, using an empty `alt` attribute is a best practice.

```html
<img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A business cat wearing
a necktie
">
```

# Link to External Page with Anchor Elements

* You can use `a` (anchor) elements to link to content outside of your web page.
  * `a` elements require **1)** A destination web address called an `href` attribute, and **2)** Anchor text.
* `target` is an optional attribute that specifies where to open the linked document.
  * Common `target` attribute values:
    * `_self` - Opens the linked document in the same frame as it was clicked (default).
    * `_blank` - Opens the linked document in a new window or tab.

```html
<a href="https://www.freecodecamp.org" target="_blank">this links to
freecodecamp.org</a>
```

# Link to Internal Sections of a Page with Anchor Elements

* `a` (anchor) elements can also be used to create internal links to jump to different sections within a webpage.
* To create an internal link, you assign a link's `href` attribute to a hash symbol `#` plus the value of the `id` attribute for the element that you want to internally link to, usually further down the page.
  * You then need to add the same `id` attribute to the element you are linking to.
    * An `id` is an attribute that uniquely describes an element.

```html
<a href=”#contacts-header”>Contacts</a>

<h2 id=”contacts-header”>Contacts</h2>
```

# Make Dead Links Using the Hash Symbol

* Sometimes you want to add `a` elements to your website before you know where they will link.
* This is also handy when you're changing the behavior of a link using JavaScript, which we'll learn about later.
* Set the `href` attribute value to `#` (hash symbol) to create a dead link.

# Create a Bulleted Unordered List

Unordered lists start with an opening `<ul>` element, followed by any number of `<li></li>` elements. Finally, unordered lists close with a `</ul>`.

```html
<ul>
	<li>Milk</li>
	<li>Cheese</li>
</ul>
```

# Create an Ordered List

Ordered lists start with an opening `<ol>` element, followed by any number of `<li></li>` elements. Finally, unordered lists close with a `</ol>`.

```html
<ol>
	<li>Milk</li>
	<li>Cheese</li>
</ol>
```

# Create a Text Field

* `input` elements are a convenient way to get input from your user.
* Note that `input` elements are **self-closing**.

```html
<input type="text">
```

# Add Placeholder Text to a Text Field

Placeholder text is what is displayed in your input element before your user has inputted anything:

```html
<input type="text" placeholder="this is the placeholder text">
```

# Create a Form Element

* You can build web forms that actually submit data to a server using nothing more than pure HTML.
  * You can do this by specifying an `action` attribute on your `form` element:

```html
<form action="/url-where-you-want-to-submit-form-data">
	<input>
</form>
```

# Add a Submit Button to a Form

Clicking this button will send the data from your form to the URL you specified with your form's `action` attribute:

```html
<button type="submit">this button submits the form</button>
```

# Use HTML5 to Require a Field

You can require specific form fields so that your user will not be able to submit your form until he or she has filled them out.

```html
<input type=”text” required>
```

# Create a Set of Radio Buttons

* You can use radio buttons for questions where you want the user to only give you one answer out of multiple options.
  * Radio buttons are a type of `input`.
* Each of your radio buttons can be nested within its own label element.
  * By wrapping an `input` element inside of a `label` element, it will automatically associate the radio button input with the `label` element surrounding it.
* All related radio buttons should have the same `name` attribute to create a radio button group.
  * By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

```html
<label>
	<input type=”radio” name=”indoor-outdoor”>Indoor
</label>
```

* **Important:** It is considered a best practice to set a `for` attribute on the label element, with a value that matches the value of the `id` attribute of the `input` element.
  * This allows assistive technologies to create a linked relationship between the label and the related `input` element.

```html
<input type=”radio” id=”indoor” name=”indoor-outdoor”>
<label for=”indoor”>Indoor</label>
```

* We can also nest the `input` element within the `label` tags:

```html
<label for=”indoor”>
	<input type=”radio” id=”indoor” name=”indoor-outdoor”>Indoor
</label>
```

# Create a Set of Checkboxes

* Forms commonly use checkboxes for questions that may have more than one answer.
  * Checkboxes are a type of `input`.
* Similar to radio buttons, each of your checkboxes can be nested within its own `label` element.
* All related checkbox inputs should have the same `name` attribute.
* **Reminder:** It is considered a best practice to explicitly define the relationship between a checkbox `input` and its corresponding `label` by setting the `for` attribute on the `label` element to match the `id` attribute of the associated `input` element.

```html
<label for=”loving”>
	<input type=”checkbox” id=”loving” name=personality>Loving
</label>
```

# Use the value attribute with Radio Buttons and Checkboxes

When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type `radio` and `checkbox` report their values from the `value` attribute.

```html
<label for=”indoor”>
	 <input type=”radio” id=”indoor” value=”indoor” name=”indoor-outdoor”>Indoor
</label>

<label for=”outdoor”>
	<input type=”radio” id=”outdoor” value=”outdoor” name=”indoor-outdoor”>Outdoor
</label>
```

* Above are two `radio` inputs:
  * When the user submits the form with the `indoor` option selected, the form data will include the line: `indoor-outdoor=indoor`. This is from the `name` and `value` attributes of the "indoor" input.
* If the `value` attribute is omitted, the submitted form data uses the default value, which is `on`. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be: `indoor-outdoor=on`, which is not useful. So the value attribute **needs** to be set to something to identify the option.

# Check Radio Buttons and Checkboxes by Default

You can set a checkbox or radio button to be checked by default using the `checked` attribute.

```html
<input type=”radio” name=”test-name” checked>
```

# Nest Many Elements within a Single div Element

* The `<div></div>` element, also known as a *division* element, is a general purpose container for other elements.
* The `div` element is probably the most commonly used HTML element of all.

# Declare the Doctype of an HTML Document

There are a few elements that give overall structure to your page, and should be included in every HTML document.

1. At the top of your document, you need to tell the browser which version of HTML your page is using.
    * You tell the browser this information by adding the `<!DOCTYPE ...>` tag on the first line, where the `...` part is the version of HTML.
    * For HTML5, you use `<!DOCTYPE html>`.
    * The `!` and uppercase `DOCTYPE` is important, especially for older browsers. The `html` is not case sensitive.

2. Next, the rest of your HTML code needs to be wrapped in `html` tags.
    * The opening `<html>` goes directly below the `<!DOCTYPE html>` line, and the closing `</html>` goes at the end of the page.

```html
<!DOCTYPE html>
<html>

</html>
```

# Define the Head and Body of an HTML Document

* You can add another level of organization in your HTML document within the `html` tags with the `head` and `body` elements.
  * Any markup with information about your page would go into the `head` tag.
    * Metadata elements, such as `link`, `meta`, `title`, and `style`, typically go inside the `head` element.
* Then any markup with the content of the page (what displays for a user) would go into the `body` tag.

```html
<!DOCTYPE html>
<html>
	<head>
	   <meta />
	</head>
	<body>
	  <div>
	  </div>
	</body>
</html>
```
