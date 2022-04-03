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

Inside that style block, you can create a CSS selector for all h2 elements:

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

