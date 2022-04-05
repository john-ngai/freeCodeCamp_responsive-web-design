# Section 2 - Basic CSS

[Responsive Web Design](https://www.freecodecamp.org/learn/responsive-web-design/) by freeCodeCamp.

# Change the Color of Text

The property that is responsible for the color of an element's text is the `color` style property.

An example of styling an individual h2 element with inline CSS (Cascading Style
Sheets):

```html
<h2 style="color: blue;">Lorem Ipsum</h2>
```

**Note:** It is a good practice to end style declarations with a `;`.

# Use CSS Selectors to Style Elements

Another, and superior, way of applying CSS is by creating a `style` block:

```html
<style>
</style>
```

Inside that style block, you can create a CSS selector for all `h2` elements:

```html
<style>
	h2 {
    color: red;
  }
</style>
```

**Note:** It's important to have both opening and closing curly braces (`{` and `}`) around each element's style rule(s).

# Use a CSS Class to Style an Element

Classes are reusable styles that can be added to HTML elements.

```html
<style>
	.blue-text {
    color: blue;
  }
</style>
```

* You can see that we've created a CSS class called `blue-text` within the `<style>` tag.
* You can apply a class to an HTML element like this: `<h2 class="blue-text">CatPhotoApp</h2>`.
  * Note that in your CSS `style` element, class names start with a period (`.`).
  * In your HTML elements' class attribute, the class name does not include the period.
* ​​Classes allow you to use the same CSS styles on multiple HTML elements.

# Change the Font Size of an Element

Font size is controlled by the `font-size` CSS property, like this:

```css
h1 {
  font-size: 30px;
}
```

# Set the Font Family of an Element

You can set which font an element should use, by using the `font-family` property:

```css
h1 {
  Font-family: sans-serif;
}
```

# Import a Google Font

* In addition to specifying common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website. 
* Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL.
* To import a Google Font, you can copy the font's URL from the Google Fonts library and then paste it in your HTML:

```html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet"
type="text/css">
```

* Now you can use the Lobster font in your CSS by using Lobster as the FAMILY_NAME as in the following example:

```css
Font-family: FAMILY_NAME, GENERIC_NAME;
```

* **Note:** The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.
* Family names are also **case-sensitive** and need to be wrapped in quotes if there is a space in the name.
  * For example, you need quotes to use the `"Open Sans"` font, but not to use the `Lobster` font.

# Specify How Fonts Should Degrade

* There are several default fonts that are available in all browsers.
  * These generic font families include `monospace`, `serif` and `sans-serif`.
* When one font isn't available, you can tell the browser to "degrade" to another font.
* For example, if you wanted an element to use the `Helvetica` font, but degrade to the `sans-serif` font when Helvetica isn't available, you will specify it as follows:

```css
p {
	  font-family: Helvetica, sans-serif;
}
```

**Note:** Generic font family names are not case-sensitive. Also, they do not need quotes
because they are CSS keywords.

# Size Your Images

CSS has a property called width that controls an element's width:

```html
<style>
	.larger-image {
    width: 500px;
  }
</style>
```

# Add Borders Around Your Elements

CSS borders have properties like style, color and width:

```html
<style>
	.thin-red-border {
    border-color: red;
	  border-width: 5px;
	  border-style: solid;
  }
</style>
```

We can also round out the corners with a CSS property called border-radius:

```css
border-radius: 10px;
```

# Give a Background Color to an Element

You can set an element's background color with the background-color property:

```css
.green-background {
  background-color: green;
}
```

# Set the id of an Element

* In addition to classes, each HTML element can also have an `id` attribute.
* There are several benefits to using `id` attributes:
  * You can use an `id` to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

```html
<h2 id=”cat-photo-app”>
```

# Use an id Attribute to Style an Element

* One cool thing about `id` attributes is that, like classes, you can style them using CSS.
* **Important:**  Unlike a `class`, an `id` is not reusable and should only be applied to one element.
  * An `id` also has a higher specificity (importance) than a `class` so if both are applied to the same element and have conflicting styles, the styles of the `id` will be applied.
* An `id` is referenced inside the style element by putting a `#` in front of their names.

```css
#cat-photo-element {
	background-color: green;
}
```

# Adjust the Padding of an Element

* You may have already noticed this, but all HTML elements are essentially little rectangles.
* Three important properties control the space that surrounds each HTML element: `padding`, `border`, and `margin`.

* An element's `padding` controls the amount of space between the element's content and its `border`.
  * When you increase an element’s `padding`, it will increase the distance (padding) between the text and the border around it.

# Adjust the Margin of an Element

* An element's `margin` controls the amount of space between an element's `border` and surrounding elements.
  * If you set an element's `margin` to a negative value, the element will grow larger.

# Add Different Padding or Margin to Each Side of an Element

* Sometimes you will want to customize an element so that it has different amounts of `padding` on each of its sides.
  * CSS allows you to control the `padding` of all four individual sides of an element with the `padding-top`, `padding-right`, `padding-bottom`, and `padding-left` properties.
* CSS also allows you to control the `margin` of all four individual sides of an element with the `margin-top`, `margin-right`, `margin-bottom`, and `margin-left` properties.

# Use Clockwise Notation to Specify the Padding or Margin of an Element

* Instead of specifying an element's `padding-top`, `padding-right`, `padding-bottom`, and `padding-left` properties individually, you can specify them all in one line, like this:

```css
padding: 10px 20px 10px 20px;
```

* These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific padding instructions.
  * The same clockwise notation also works for specifying an element’s `margin-top`, `margin-right`, `margin-bottom`, and `margin-left` properties all in one line.

# Use Attribute Selectors to Style Elements

* You have been adding `id` or `class` attributes to elements that you wish to specifically style. These are known as ID and class selectors.
  * There are other CSS Selectors you can use to select custom groups of elements to style.

For example, the `[attr=value]` attribute selector matches and styles elements with a specific attribute value.

```css
[type=”radio”] {
	margin: 20px 0px 20px 0px;
}
```

# Understand Absolute versus Relative Units

* Pixels (`px`) are a type of length unit, which is what tells the browser how to size or space an item.
  * In addition to `px`, CSS has a number of different length unit options that you can use.

* The two main types of length units are *absolute* and *relative*:
  * Absolute units tie to physical units of length.
    * For example, `in` and `mm` refer to inches and millimeters, respectively. 
    * Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.
  * Relative units, such as `em` or `rem`, are relative to another length value.
    * For example, `em` is based on the size of an element's font.
    * If you use it to set the `font-size` property itself, it's relative to the parent's `font-size`.

# CSS Inheritance

* Every HTML page has a `body` element.
* We can prove that the `body` element exists here by giving it a `background-color` of `black`, even when a `body` element isn’t explicitly declared.
* As such, any elements declared within the `body` will also inherit the styles applied to it.

# Prioritize One Style Over Another

* Sometimes your HTML elements will receive multiple styles that conflict with one another.
  * For example, an `h1` element can't be both `green` and `pink` at the same time.
* `class` CSS declaration will override regular element CSS declarations.
  * The most recently declared `class` declarations will also override previously declared `class` declarations.
* Similarly, an `id` CSS declaration will override a `class` CSS declaration.
* Next, an inline declaration will override both an `id` and `class` declaration.

* Finally, the keyword `!important` will override all other CSS declarations.
  * In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use `!important`.

```css
.pink-text {
	color: pink !important;
}
```

# Use Hex Code for Specific Colors

* One other way to represent colors in CSS is called hexadecimal code, or hex code for short.
  * We usually use decimals, or base 10 numbers, which use the symbols 0 to 9 for each digit. Hexadecimals (or hex) are base 16 numbers.
    * This means it uses sixteen distinct symbols. Like decimals, the symbols 0-9 represent the values zero to nine. Then A,B,C,D,E,F represent the values ten to fifteen.
    * Altogether, 0 to F can represent a digit in hexadecimal, giving us 16 total possible values.
    * You can find more information about [hexadecimal numbers here](https://www.freecodecamp.org/news/hexadecimal-number-system/).

* In CSS, we can use 6 hexadecimal digits to represent colors, two each for the red (R), green (G), and blue (B) components
  * For example, `#000000` is black and is also the lowest possible value.
  * You can find more information about the [RGB color system here](https://www.freecodecamp.org/news/rgb-color-html-and-css-guide/#whatisthergbcolormodel).

# Use Hex Code to Mix Colors

* From the three pure colors (red, green, and blue) used in hex code, we can vary the amounts of each to create over 16 million other colors!
  * For example, orange is pure red, mixed with some green, and no blue. In hex code, this translates to being `#FFA500`.
* The digit `0` is the lowest number in hex code, and represents a complete absence of color.
* The digit `F` is the highest number in hex code, and represents the maximum possible brightness.

# Use Abbreviated Hex Code

* Many people feel overwhelmed by the possibilities of more than 16 million colors. And it's difficult to remember hex code. Fortunately, you can shorten it.
  * For example, red's hex code `#FF0000` can be shortened to `#F00`. This shortened form gives one digit for red, one digit for green, and one digit for blue.
    * This reduces the total number of possible colors to around 4,000. But browsers will interpret `#FF0000` and `#F00` as exactly the same color.
  
# Use RGB values to Color Elements

* Another way you can represent colors in CSS is by using RGB values.
* The RGB value for black looks like this:

`rgb(0, 0, 0)`

* The RGB value for white looks like this:

`rgb(255, 255, 255)`

* Instead of using six hexadecimal digits like you do with hex code, with RGB you specify the brightness of each color with a number between `0` and `255`.

# Use RGB to Mix Colors

Just like with hex code, you can mix colors in RGB by using combinations of different values.

**e.g.**

Blue - `rgb(0, 0, 255)`<br>
Red - `rgb(255, 0, 0)`<br>
Orchid - `rgb(218, 112, 214)`<br>
Sienna - `rgb(160, 82, 45)`

# Use CSS Variables to change several elements at once

*CSS Variables* are a powerful way to change many CSS style properties at once by changing only one value.

```css
--penguin-skin: black;

.penguin-top {
	background: var(--penguin-skin, gray);
}
```

# Create a custom CSS Variable

To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:
	
```css
--penguin-skin: gray;
```

This will create a variable named `--penguin-skin` and assign it the value of `gray`.

# Use a custom CSS Variable

After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it:

```css
background: var(--penguin-skin);
```

This will change the background of whatever element you are targeting to `gray` because that is the value of the `--penguin-skin` variable.

# Attach a Fallback value to a CSS Variable

When using your variable as a CSS property value, you can attach a fallback value that your browser will revert to if the given variable is invalid.

**Note:** This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.

```css
background: var(--penguin-skin, black);
```

This will set the background to `black` if your variable wasn't set. Note that this can be useful for debugging.

# Improve Compatibility with Browser Fallbacks

* When working with CSS you will likely run into browser compatibility issues at some point. This is why it's important to provide browser fallbacks to avoid potential problems.
* When your browser parses the CSS of a webpage, it ignores any properties that it doesn't recognize or support.
  * In that case, the browser will use whatever value it has for that property. If it can't find any other value set for that property, it will revert to the default value, which is typically not ideal.
  * This means that if you do want to provide a browser fallback, it's as easy as providing another more widely supported value immediately before your declaration. 
    * That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.

**Example**

Improve the browser’s compatibility by adding another background declaration right
before the existing declaration and set its value to `red`.

```css
.red-box {
  background: red;
  background: var(--red-color);
}
```

# Inherit CSS Variables

* When you create a variable, it is available for you to use inside the selector in which you create it.
  * It also is available in any of that selector's descendants. This happens because CSS variables are inherited, just like ordinary properties.

* To make use of inheritance, CSS variables are often defined in the `:root` element.
  * `:root` is a pseudo-class selector that matches the root element of the document, usually the `html` element. 
  * By creating your variables in `:root`, they will be available globally and can be accessed from any other selector in the style sheet.
    * You can then overwrite these variables by setting them again within a specific element.

# Use a media query to change a variable

* CSS Variables can simplify the way you use media queries.
* For instance, when your screen is smaller or larger than your media query breakpoint, you can change the value of a variable, and it will apply its style wherever it is used.

```css
@media (max-width: 350px) {
	:root {
	  --penguin-size: 200px;
	  --penguin-skin: black;
  }
}
```
