# Section 3 - Applied Visual Design

[Responsive Web Design](https://www.freecodecamp.org/learn/responsive-web-design/) by freeCodeCamp.

# Create Visual Balance Using the text-align Property

* Text is often a large part of web content.
* CSS has several options for how to align it with the text-align property:
  * `text-align: justify;` spaces the text so that each line has equal width,
  * `text-align: center;` centers the text,
  * `text-align: right;` right-aligns the text,
  * and `text-align: left;` (the default) left-aligns the text.

# Adjust the Width and Height of an Element Using the width Property

You can specify the width of an element using the width property in CSS:

```css
.fullcard {
	  width: 200px;
	  height: 400px;
}
```

# Use the strong Tag to Make Text Bold

* To make text bold, you can use the `strong` tag.
  * This is often used to draw attention to text and symbolize that it is important.
* With the `strong` tag, the browser applies the CSS of `font-weight: bold;` to the element.

```html
<p>
  <strong>Lorem Ipsum</strong>
</p>
```

# Use the u Tag to Underline Text

* To underline text, you can use the `u` tag.
  * This is often used to signify that a section of text is important, or something to remember.
* With the `u` tag, the browser applies the CSS of `text-decoration: underline;` to the element.

# Use the em Tag to Italicize Text

* To emphasize text, you can use the `em` tag.
* This displays text as italicized, as the browser applies the CSS of `font-style: italic;` to the element.

# Use the s Tag to Strikethrough Text

* To strikethrough text, which is when a horizontal line cuts across the characters, you can use the `s` tag.
* It shows that a section of text is no longer valid. With the `s` tag, the browser applies the CSS of `text-decoration: line-through;` to the element.

# Create a Horizontal Line Using the hr Element

* You can use the `hr` tag to add a horizontal line across the width of its containing element.
  * This can be used to define a change in topic or to visually separate groups of content.
* **Note:** The `hr` tag is self-enclosing.

# Adjust the background-color Property of Text

* Instead of adjusting your overall background or the color of the text to make the foreground easily readable, you can add a `background-color` to the element holding the text you want to emphasize.
  * The following example uses `rgba()` colors:
    * r = red, g = green, b = blue, a = alpha/level of opacity.
    * rgb values range from `1` to `255`.
    * The alpha value ranges from `1` (solid/opaque) to `0` (transparent).

```css
h1 {
	background-color: rgba(45, 45, 45, 0.1);
}
```

# Adjust the Font Size of the Text in an Element

You use the `font-size` property to adjust the size of the text in an element:

```css
h2 {
	font-size: 27px;
}
```

# Add a box-shadow to a Card-like Element

* The `box-shadow` property applies one or more shadows to an element.
* The `box-shadow` property takes values for:
1. `offset-x` (how far to push the shadow horizontally from the element),
2. `offset-y` (how far to push the shadow vertically from the element),
3. `blur-radius`,
4. `spread-radius` (optional) and
5. `color` (optional), in that order.

* Multiple box-shadows can be also created by using commas to separate properties of each `box-shadow` element.

An example of the CSS to create multiple shadows with some blur, at mostly-transparent
black colors.

```css
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```

# Decrease the Opacity of an Element

* The `opacity` property in CSS is used to adjust the opacity, or conversely, the transparency for an item.
  * The `opacity` value ranges between `1` (solid/opaque) to `0` (transparent).
* The value given will apply to the entire element, whether that's an image with some transparency, or the foreground and background colors for a block of text.

# Use the text-transform Property to Make Text Uppercase

* The `text-transform` property in CSS is used to change the appearance of text.
  * It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.

The following table shows how the different `text-transform` values change the example text "Transform me".

| **Value** |  **Result**  |
|-----------|--------------|
|lowercase  |"transform me"|
|uppercase  |"TRANSFORM ME"|
|capitalize |"Transform Me"|
|initial    |(default)     |
|inherit    |(parent)      |
|none       |(default)     |

# Set the Font Weight for An Element

* The `font-weight` property sets how thick or thin characters are in a section of text.
  * A common property value for `font-weight` are values between `100` to `900`, from thin to thick characters.
    * A value of `400` is the same as normal.

# Set the line-height of Paragraphs

* CSS offers the `line-height` property to change the height of each line in a block of text.
  * As the name suggests, it changes the amount of vertical space that each line of text gets.

# Adjust the Hover State of an Anchor Tag

* A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.
  * For example, the styling of an anchor tag can be changed for its hover state using the `:hover` pseudo-class selector.

```css
a:hover {
  color: red;
}
```

# Change an Element's Relative Position

* CSS treats each HTML element as its own box, which is usually referred to as the *CSS Box Model*.
* Block-level items automatically start on a new line (think headings, paragraphs, and divs) while inline items sit within surrounding content (like images or spans).
* The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

* When the position of an element is set to relative, it allows you to specify how CSS should move it relative to its current position in the normal flow of the page.
  * It pairs with the CSS offset properties of `left` or `right`, and `top` or `bottom`.
    * These say how many pixels, percentages, or ems to move the item away from where it is normally positioned (effectively, the opposite direction).
  * Changing an element's position to relative does not remove it from the normal flow - other elements around it still behave as if that item were in its default position.

* **Note:** Positioning gives you a lot of flexibility and power over the visual layout of a page. It's good to remember that no matter the position of elements, the underlying HTML markup should be organized and make sense when read from top to bottom. This is how users with visual impairments (who rely on assistive devices like screen readers) access your content.

```css
p {
	position: relative;
	bottom: 10px;
}
```

# Lock an Element to its Parent with Absolute Positioning

* The next option for the CSS `position` property is `absolute`, which locks the element in place relative to its parent container.
  * Unlike the `relative` position, this **removes** the element from the normal flow of the document, so surrounding items ignore it.
* One nuance with absolute positioning is that it will be locked relative to its closest positioned ancestor.
  * **Important:** If you forget to add a position rule to the parent item, (this is typically done using `position: relative;`), the browser will keep looking up the chain and ultimately default to the `body` tag.

# Lock an Element to the Browser Window with Fixed Positioning

* The next layout scheme that CSS offers is the `fixed` position, which is a type of absolute positioning that locks an element relative to the browser window.
  * Similar to `absolute` positioning, it's used with the CSS offset properties and also removes the element from the normal flow of the document.
  * Other items no longer "realize" where it is positioned, which may require some layout adjustments elsewhere.
* One key difference between the fixed and absolute positions is that an element with a fixed position won't move when the user scrolls.

# Push Elements Left or Right with the float Property

* The next positioning tool does not actually use position, but sets the float property of an element.
* Floating elements are removed from the normal flow of a document and pushed to either the left or right of their containing parent element.
  * It's commonly used with the width property to specify how much horizontal space the floated element requires.

```css
section {
	float: left;
}
```

# Change the Position of Overlapping Elements with the z-index Property

* When elements are positioned to overlap (i.e. using `position: absolute` | `relative` | `fixed` | `sticky`), the element coming later in the HTML markup will, by default, appear on the top of the other elements. 
  * However, the `z-index` property can specify the order of how elements are stacked on top of one another.
    * It must be an integer (i.e. a whole number and not a decimal), and higher values for the `z-index` property of an element move it higher in the stack than those with lower values.

```css
.first {
  background-color: red;
  position: absolute;
  z-index: 2;
}

.second {
  background-color: blue;
  position: absolute;
  left: 40px;
  right: 50px;
  z-index: 1;
}
```

* Without the `z-index`, the element with the class name of `first` would appear behind the element with the class name of `second`.

# Center an Element Horizontally Using the margin Property

* Another positioning technique is to center a block element horizontally. One way to do this is to set its `margin` to a value of `auto`.
* This method works for images, too. **Images are inline elements by default**, but can be changed to block elements when you set the `display` property to `block`.

```css
div {
  background-color: blue;
  height: 100px;
  width: 100px;
  margin: auto;
}
```

# Learn about Complementary Colors

* The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. 
  * When two colors are opposite each other on the wheel, they are called complementary colors.
    * They have the characteristic where, if combined, they "cancel" each other out and create a gray color.
    * However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast.
  * Some examples of complementary colors with their hex codes are:
    * red (#FF0000) and cyan (#00FFFF),
    * green (#00FF00) and magenta (#FF00FF),
    * blue (#0000FF) and yellow (#FFFF00).
* Modern color theory uses the additive RGB model (like on a computer screen) and the subtractive CMY(K) model (like in printing).
  * Read the [Color Model Wiki page](https://en.wikipedia.org/wiki/Color_model) for more information on this complex subject.

# Learn about Tertiary Colors

* Computer monitors and device screens create different colors by combining amounts of red, green, and blue light.
  * This is known as the RGB additive color model in modern color theory.
  * Red (R), green (G), and blue (B) are called primary colors.
    * Mixing two primary colors creates the secondary colors cyan (G + B), magenta (R + B) and yellow (R + G).
      * These secondary colors happen to be the complement to the primary color not used in their creation, and are opposite to that primary color on the color wheel.
      * For example, magenta is made with red and blue, and is the complement to green.
* Tertiary colors are the result of combining a primary color with one of its secondary color neighbors.
  * For example, within the RGB color model, red (primary) and yellow (secondary) make orange (tertiary).
    * This adds six more colors to a simple color wheel for a total of twelve.
* There are various methods of selecting different colors that result in a harmonious combination in design.
  * One example that can use tertiary colors is called the split-complementary color scheme. This scheme starts with a base color, then pairs it with the two colors that are adjacent to its complement.
    * The three colors provide strong visual contrast in a design, but are more subtle than using two complementary colors.
  * Here are three colors created using the split-complement scheme:
    * orange	#FF7F00,
    * cyan #00FFFF,
    * raspberry #FF007F.

# Adjust the Hue of a Color

* Colors have several characteristics including hue, saturation, and lightness.
  * CSS3 introduced the `hsl()` property as an alternative way to pick a color by directly stating these characteristics.
* **Hue** is what people generally think of as 'color'.
  * If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line.
  * In `hsl()`, hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between `0` and `360`.
* **Saturation** is the amount of gray in a color.
  * A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray.
  * This is given as a percentage with `100%` being fully saturated.
* **Lightness** is the amount of white or black in a color.
  * A percentage is given ranging from `0%` (black) to `100%` (white), where `50%` is the normal color.

red - `hsl(0, 100%, 50%)` <br>
yellow - `hsl(60, 100%, 50%)` <br>
green - `hsl(120, 100%, 50%)`

# Adjust the Tone of a Color

* The `hsl()` option in CSS also makes it easy to adjust the tone of a color.
  * Mixing white with a pure hue creates a **tint** of that color, and adding black will make a **shade**.
  * Alternatively, a **tone** is produced by adding gray or by both tinting and shading.

# Create a Gradual CSS Linear Gradient

* CSS provides the ability to use color transitions, otherwise known as gradients, on elements.
  * This is accessed through the `background` property's `linear-gradient()` function.
* Here is the general syntax:

```css
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
```

* The first argument specifies the direction from which color transition starts - it can be stated as a degree, where `90deg` makes a horizontal gradient (from left to right) and `45deg` makes a diagonal gradient (from bottom left to top right).

```css
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
```

# Use a CSS Linear Gradient to Create a Striped Element

* The `repeating-linear-gradient()` function is very similar to `linear-gradient()` with the major difference that it repeats the specified gradient pattern.
  * `repeating-linear-gradient()` accepts a variety of values, but for simplicity, this example only illustrates the angle value and color stop values.
    * The angle value is the direction of the gradient.
    * Color stops are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.

```css
repeating-linear-gradient(
  90deg,
  yellow 0px,
  blue 40px,
  green 40px,
  red 80px
);
```

![Illustration of a repeating linear gradient](https://github.com/mrjohnming/freeCodeCamp_responsive-web-design/blob/main/docs/repeating-linear-gradient.png)

* The gradient starts with the color `yellow` at `0px`, which blends into the second color `blue` at `40px` away from the start.
* Since the next color stop is also at `40px`, the gradient immediately changes to the third color `green`, which itself blends into the fourth color value `red` as that is `80px` away from the beginning of the gradient.
* For this example, it helps to think about the color stops as pairs where every two colors blend together:
  * 0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px
    * If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.
