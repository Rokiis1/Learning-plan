# Table of Contents

- [Basics CSS](#basics-css)
- [Selectors](#selectors)
- [CSS Properties](#css-properties)
- [CSS Units](#css-units)
- [Width And Length](#width-and-length)
- [CSS Fonts](#font)
- [CSS Color Formats](css-color-formats)
- [CSS Layout](#css-layout)
- [Media Queries](#media-queries)

# CSS

## Introduction to CSS

CSS stands for Cascading Style Sheets and is a stylesheet language used to define the visual presentation of HTML and XML documents. It allows you to control the layout, colors, fonts, and other visual aspects of a web page.

```html
<link rel="stylesheet" type="text/css" href="styles.css">
```

## CSS Syntax

CSS rules consist of a selector and a declaration block. The selector identifies the HTML element(s) to style, and the declaration block contains one or more declarations separated by semicolons. Each declaration consists of a property and a value.

```css
selector {
  property: value;
  property: value;
  /* more declarations... */
}
```

## BEM architecture

Explain the BEM (Block, Element, Modifier) architecture and how it is utilized in your project. Describe the purpose and structure of blocks, elements, and modifiers, and how they interact with each other. Provide examples to demonstrate the BEM naming conventions and guidelines followed in your project.

```css
/* Block */
.button {
  display: inline-block;
  padding: 10px 20px;
  background-color: #f0f0f0;
  color: #333;
  font-weight: bold;
  text-decoration: none;
  border: none;
}

/* Element */
.button__icon {
  display: inline-block;
  margin-right: 5px;
}

/* Modifier */
.button--primary {
  background-color: #007bff;
  color: #fff;
}

.button--large {
  padding: 15px 30px;
  font-size: 1.2em;
}

.button--large-tag {
  /* Additional modifier styles */
  border-radius: 5px;
}
```

### Why should you use BEM?

- Modularity: BEM encourages a modular approach to CSS, making it easier to manage and scale your stylesheets. The block, element, and modifier structure promotes code reuse and separation of concerns.

- Readability: BEM provides a clear and descriptive naming convention. It makes your code more readable and self-explanatory, reducing confusion and improving collaboration among developers.

- Maintainability: With BEM, you have a predictable and structured way of writing CSS. This improves code maintainability as it becomes easier to locate, modify, and update specific styles or components.

- Scalability: BEM is particularly useful for large-scale projects where multiple developers are working together. Its naming conventions and modular structure make it easier to manage and extend the codebase without introducing conflicts or unintended side effects.

### Resource

- [(Article)BEM methodology](https://en.bem.info/methodology/quick-start/)

# Selectors

Selectors are used to target specific HTML elements to apply styles. Here are some commonly used selectors:

## Basic Selectors

### Element Selector

- Element Selector: Selects elements based on their HTML tag name. For example, `p` selects all `<p>` elements.

```html
<p>This is a paragraph.</p>
```
```css
p {
  property: value;
  property: value;
  /* more declarations... */
}
```
### Class Selector

- Class Selector: Selects elements based on their class attribute. It uses a dot (`.`) followed by the class name. For example, `.my-class` selects all elements with the class "my-class".

```html
  <p class="highlight">This is a paragraph with a class of "highlight".</p>
```
```css
.highlight {
  property: value;
  property: value;
  /* more declarations... */
}
```
### ID Selector

- ID Selector: Selects a single element based on its ID attribute. It uses a hash (`#`) followed by the ID name. For example, `#my-id` selects the element with the ID "my-id".

```html
<div id="box">This is a div with an ID of "box".</div>
```
```css

#box {
  property: value;
  property: value;
  /* more declarations... */
}

```
### Inline selector

- Inline selector: In HTML are defined directly within the HTML elements using the `style` attribute. Here's an example of how inline styles look in HTML:

```html
<div style="property: value;">This is a box</div>
```
### Descendant Selector

- Descendant Selector: Targets elements that are descendants of another element.

```html
  <section class="parent">
    <h1>This is the parent element</h1>
    <p>This is a paragraph inside the parent element.</p>
    <article>
      <p>This is a paragraph inside a nested div.</p>
      <span>This is a span element inside the nested div.</span>
    </article>
  </section>
```
```css
.parent p {
  /* CSS properties */
  property: value;
}

.parent span {
  /* CSS properties */
  property: value;
}
```

### Universal Selector

- Universal Selector: Selects all elements on the page. It uses an asterisk (`*`). For example, `*` selects all elements.

```css
* {
  /* CSS properties */
  property: value;
}
```

# CSS Properties

CSS properties define the visual appearance of HTML elements. Some commonly used properties include:

- `width`: Specifies the width of an element.
- `height`: Specifies the height of an element.
- `margin`: Specifies the margin around an element.
- `padding`: Specifies the padding within an element.
- `font-size`: Specifies the size of the font.
- `font-weight`: Specifies the weight or thickness of the font.
- `line-height`: Specifies the height of a line of text.
- `font-family`: Specifies the font family or list of font families for text.
- `border-radius`: Specifies the radius of the border corners.
- `border`: Specifies the border around an element.
- `color`: Specifies the text color.
- `background-color`: Specifies the background color.
- `display`: Specifies how an element should be displayed (e.g., block, inline, inline-block).

## CSS Units

CSS supports various units for specifying measurements. Some common units include pixels (px), percentages (%), em, rem, and viewport units (vw, vh). Understanding and using the appropriate units is important for creating responsive and scalable designs.

### Pixels (px):

- When you need precise control over element sizes or positioning.
- When working with fixed-width elements that should maintain a consistent size across different devices.
- Example: Setting the width of a container to 300 pixels: `.container { width: 300px; }`

### Percentages (%):

- When you want elements to scale proportionally based on the size of their parent container.
- When creating fluid layouts that adapt to different screen sizes.
- Example: Setting the width of a child element to 50% of its parent: `.child { width: 50%; }`

### EM:

- When you want to define sizes relative to the font size of the parent element.
- Useful for creating scalable typography.
- Example: Setting the font size of a paragraph to 1.2 times the font size of its parent: `.parent { font-size: 16px; } .child { font-size: 1.2em; }`

### REM:

- Similar to EM, but relative to the root (html) element's font size.
- Useful for creating scalable layouts and consistent spacing.
- Example: Setting the margin of an element to 1.5 times the root font size: `.element { margin: 1.5rem; }`

### Viewport units (vw, vh):

- When you want to size elements relative to the viewport's width or height.
- Useful for creating responsive designs that adapt to different screen sizes.
- Example: Setting the height of an element to 50% of the viewport height: `.element { height: 50vh; }`

# Width And Length

## `<html>` vs `<body>`

- In HTML, the `<html>` tag is the root element of the document, encapsulating the entire content. It represents the HTML document as a whole. This tag is usually placed at the beginning and end of an HTML file.

- The `<body>` tag, on the other hand, represents the main content of the HTML document. It contains all the visible elements that users see when they visit a web page. The `<body>` tag is nested inside the `<html>` tag and typically follows the `<head>` tag, which contains meta information and scripts.

## How backgorund-color works on html and body tags

-  By default, the background color set on the `<html>` tag will apply to the entire page, including areas where there is no content. This means that the background color will extend beyond the visible content of the page. However, when you set the background color on the `<body>` tag, it will only apply to the area containing the actual content of the page. The background color will not extend beyond the content area.

### CSS Font

#### Font sample

```css
@import url('https://fonts.googleapis.com/css?family=Roboto');

.sample-text {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  font-weight: bold;
  line-height: 1.5;
}

```

### (Optional)CSS Color Formats

In CSS, there are several color formats you can use to specify colors.

#### Hexadecimal Colors

Hexadecimal colors are represented using a combination of six alphanumeric characters (`#RRGGBB`), where `RR` represents the red value, `GG` represents the green value, and `BB` represents the blue value. For example, `#FF0000` represents pure red.

Hexadecimal colors are widely used in CSS because they provide a large range of colors and are supported by all modern browsers.

```css

/* Hexadecimal Colors */
.hex-color {
  color: #FF0000; /* Red */
  background-color: #00FF00; /* Green */
  border: 2px solid #0000FF; /* Blue border */
  box-shadow: 2px 2px 4px #888888; /* Gray shadow */
}
```

#### Hexadecimal Colors with Transparency

To add transparency to a hexadecimal color, you can use an additional two-digit value at the end of the color code (`#RRGGBBAA`), where `AA` represents the `alpha` or transparency value. For example, `#FF0000FF` represents opaque red, and `#FF000080` represents semi-transparent red.

This format allows you to control the opacity of a color, making it useful for overlays, gradients, and other visual effects.

```css
/* Hexadecimal Colors with Transparency */
.hex-color-transparent {
  color: #FF0000FF; /* Opaque Red */
  background-color: #FF000080; /* Semi-transparent Red */
  border: 2px solid #00FFFF80; /* Semi-transparent Cyan border */
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); /* Semi-transparent black shadow */
}

```

#### RGB Colors

RGB colors are represented using three numeric values for red, green, and blue, respectively (`rgb(R, G, B)`). Each value ranges from `0` to `255`, representing the intensity of each color channel. For example, `rgb(255, 0, 0)` represents pure red.

RGB colors provide a convenient way to specify colors using familiar numeric values, making them easy to understand and manipulate.

```css
/* RGB Colors */
.rgb-color {
  color: rgb(255, 0, 0); /* Red */
  background-color: rgb(0, 255, 0); /* Green */
  border: 2px solid rgb(0, 0, 255); /* Blue border */
  box-shadow: 2px 2px 4px rgb(136, 136, 136); /* Gray shadow */
}

```

#### RGBA Colors

Similar to `RGB` colors, `RGBA` colors also represent red, green, and blue values, but with an additional alpha value for transparency (`rgba(R, G, B, A)`). The alpha value ranges from `0` to `1`, where `0` represents fully transparent and `1` represents fully opaque. For example, rgba`(255, 0, 0, 0.5)` represents semi-transparent red.

`RGBA` colors are useful when you need to control the transparency of a color without affecting other elements on the page.

```css
/* RGBA Colors */
.rgba-color {
  color: rgba(255, 0, 0, 0.5); /* Semi-transparent Red */
  background-color: rgba(0, 255, 0, 0.2); /* Semi-transparent Green */
  border: 2px solid rgba(0, 0, 255, 0.8); /* Semi-transparent Blue border */
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* Semi-transparent black shadow */
}

```

#### HSL Colors

`HSL` stands for Hue, Saturation, and Lightness. `HSL` colors use three values: hue (`0 to 360 degrees`), saturation (`0% to 100%`), and lightness (`0% to 100%`) (`hsl(H, S, L)`). Hue represents the color itself, saturation controls the intensity, and lightness determines how light or dark the color is.

HSL colors offer a more intuitive way to manipulate colors, allowing you to adjust hue, saturation, and lightness independently.

```css
/* HSL Colors */
.hsl-color {
  color: hsl(0, 100%, 50%); /* Red */
  background-color: hsl(120, 100%, 50%); /* Green */
  border: 2px solid hsl(240, 100%, 50%); /* Blue border */
  box-shadow: 2px 2px 4px hsl(0, 0%, 53%); /* Gray shadow */
}
```

#### Examples

[Example](https://codesandbox.io/s/kind-feather-wjju44?file=/index.html)

# CSS Layout

**Explanation:**

**CSS (Cascading Style Sheets) Layout** refers to the technique of positioning and arranging elements on a web page. It plays a crucial role in determining how content is displayed and organized in a web document. CSS Layout enables web designers and developers to control the placement, size, and spacing of elements such as text, images, and other HTML elements within a webpage.

![CSS Layouts](./assets/images/cssLayouts/cssLayout.png)

## Box Model

**Explanation:**

 The foundation of CSS layout is the box model. In this model, every element on a webpage is treated as a rectangular box. Each box comprises four core properties: content, padding, border, and margin. These properties collectively dictate the element's size and positioning within the layout.

![Box model](./assets/images/cssLayouts/boxModel.png)

- [CSS Box-Model Diagram](#css-box-model-diagram)
- [Margins vs Padding Property](#margins-vs-padding-property)
- [Border Property](#border-property)
- [Box-sizing Property](#box-sizing-property)

### CSS Box-Model Diagram

**Explanation:**

Think of the CSS box-model like an *onion*. It has **4 Layers:**

- **1st layer:** Content

- **2nd layer:** Padding

- **3rd layer:** Border

- **4th layer:** Margin

![Box Model Diagram](./assets/images/cssLayouts/boxModelDiagram.png)

**Example:**

- [Example: CSS Box-Model Diagram](https://codesandbox.io/s/boxmodel-dgyxtj?file=/index.html)

### Margins vs Padding Property

**Explanation:**

**Margins and Padding** are fundamental properties in CSS that control the spacing around and within HTML elements, playing a critical role in the layout and design of web pages. They are used to create space, alignment, and separation between elements.

**Key Concepts:**

- **Margins:** Margins are the spaces outside an element. They define the gap between the element and its adjacent elements. Margins do not have a background color or content, and they effectively separate elements from one another or from the edges of their containing element.

- **Padding:** Padding, on the other hand, is the space within an element, between the element's content and its border. Padding is used to control the distance between an element's content and its border. It affects the size and spacing of the element's content.

**Syntax:**

```css
/* Margin: margin-top margin-right margin-bottom margin-left; */
/* Margin can be set using auto, a length value, a percentage, or other units. */
selector {
    margin: 10px 20px 10px 30px; /* Example setting margins for top, right, bottom, and left sides */
}

/* Padding: padding-top padding-right padding-bottom padding-left; */
/* Padding can also be set using various units and values. */
selector {
    padding: 5% 15px 0 0; /* Example setting padding for top, right, bottom, and left sides */
}
```

### Border Property

**Explanation:**

The `border` property in CSS is used to define the style, width, and color of an element's border. It plays a significant role in the visual design and layout of web pages, helping to create distinctions between elements and improve overall aesthetics.

**Key Concepts:**

1. **Border Style:** The `border-style` property determines the type of border to be displayed. Common values include `solid`, `dotted`, `dashed`, `double`, `none`.

2. **Border Width:** The `border-width` property specifies the thickness of the border. It can take values like `thin`, `medium`, `thick`, or specific measurements in pixels (`px`), `em`, `rem`, etc. You can set different widths for each border side (top, right, bottom, left) or use shorthand notations.

3. **Border Color:** The `border-color` property defines the color of the border. It can accept color names, hexadecimal color codes, RGB values, or other valid color representations. Like border width, you can set different colors for each side or use shorthand notations.

**Syntax:**

```css
selector {
    border: border-style border-width border-color;
}
```

**Example:**

- [Example: Border Property](https://codesandbox.io/s/boxmodelborders-57fz7y?file=/index.html)

### Box-sizing Property

**Explanation:**

The `box-sizing property` in CSS is used to control how an element's total width and height are calculated, particularly in relation to its content, padding, and border. Understanding and using this property is crucial for managing the layout of web elements. 

**Key Concepts:**

- **Content Box (default):** By default, the `box-sizing` property is set to `content-box`. In this mode, an element's width and height only consider the content itself. Padding and border are added to the specified width and height.

- **Border Box:** When `box-sizing` is set to `border-box`, the width and height of an element include the content, padding, and border. This means that the padding and border dimensions are included within the specified width and height, and the content area shrinks accordingly.

**Syntax:**

```css
selector {
    box-sizing: content-box; /* or box-sizing: border-box; */
}
```

## Floats

**Explanation:**

The CSS Float Property is a fundamental feature in CSS that allows elements to float to the left or right within their container, causing other elements to flow around them. This property is commonly used for creating text wrapping around images or positioning elements side by side.

**Key Concepts:**

- **Float Property:** The `float` property is used to specify whether an element should be floated to the left, right, or not at all. It is typically applied to block-level elements like images and divs.

- **Text Wrapping:** When an element is floated, adjacent text and inline elements will wrap around it, filling the available space beside the floated element.

- **Clear Property:** To prevent elements from floating around a floated element, you can use the `clear` property to ensure that no floating elements are allowed on a specific side of the cleared element.

**Syntax:**

```css
selector {
    float: left | right | none | inherit;
}
```
- **left:** The element floats to the left.
- **right:** The element floats to the right.
- **none:** The element does not float, and content flows around it as normal.
- **inherit:** The element inherits the float property from its parent.

**Example:**

- [Example: Float 1](https://codesandbox.io/s/float-j56g3x?file=/index.html)

- [Example: Float 2](https://codesandbox.io/s/float-jpg-mmzccy?file=/styles.css)

## Position property:

- `static` (default): Elements are rendered in their normal order and flow within the document.
- `relative`: Elements are positioned `relative` to their normal position. You can use properties like `top`, `bottom`, `left`, or `right` to offset them from their original position.
- `absolute`: Elements are positioned `relative` to their nearest positioned ancestor. If there is no positioned ancestor, it's positioned `relative` to the initial containing block.
- `fixed`: Elements are positioned `relative` to the browser window and do not move even if the page is scrolled.

## Positioning and Z-index

- In HTML and CSS, you can use the position property to define how an element is positioned on a web page. There are several possible values for the position property, including `static` (the default), `relative`, `absolute`, and "`fixed`.

When you set the position property to `relative` or `absolute`, you can use the `z-index` property to control the stacking order of elements. The `z-index` property determines which element appears in front or behind other elements when they overlap on the page.

Explanation of how the position property and `z-index` work together:


## Z-index property:

- The `z-index` property is used to specify the stack order of positioned elements.
- It takes a numeric value, where elements with a higher `z-index` value appear in front of elements with a lower value.
- Negative values are also allowed, and elements with negative `z-index` values appear behind elements with positive values or the default stack order.

## Code example

- [Fixed possition](https://codesandbox.io/s/fixedposistion-rm9xr6)
- [Relative and Absolute position](https://codesandbox.io/s/relative-and-absolute-position-m6226x)
- [z-index](https://codesandbox.io/s/vigorous-smoke-wqrz6c?file=/index.html)

## Flexbox

- [Getting Started](#flex-box-getting-started)
- [Flex Container](#flex-container)
- [Flex Items](#flex-items)
- [Flex Direction](#flex-directions)
- [Justify Content](#justify-content)
- [Align Items](#align-items)
- [Flex Wrap](#flex-wrap

Flexbox is a CSS layout module that provides an efficient way to arrange and align elements within a container. It offers a flexible and responsive design approach, making it ideal for building user interfaces.

### Getting Started

To use Flexbox, you need to define a flex container by setting the `display` property of the container to `flex`. This enables the container to arrange its child elements using Flexbox.

```css
.container {
  display: flex;
}
```

### Flex Container

The flex container is the parent element that holds the flex items. It defines the context in which Flexbox layout operates. Here are a few properties commonly used with flex containers:

`flex-direction`: Specifies the direction in which the flex items are laid out.
`justify-content`: Defines how flex items are aligned along the main axis.
`align-items`: Sets the alignment of flex items along the cross axis.
`flex-wrap`: Determines whether flex items should wrap or remain on a single line.

### Flex Items

Flex items are the child elements within the flex container. They are laid out based on the properties set on the flex container. Here's an example of a flex container with three flex items:

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```
```css
.container {
  display: flex;
}

.item {
  /* Add styling properties to the flex items */
}
```

### Flex Direction

The `flex-direction` property controls the direction in which flex items are laid out. It accepts four possible values:

`row`: Flex items are laid out horizontally from left to right.
`row-reverse`: Flex items are laid out horizontally from right to left.
`column`: Flex items are laid out vertically from top to bottom.
`column-reverse`: Flex items are laid out vertically from bottom to top.

```css
.container {
  flex-direction: value;
}
```
### Justify Content

The `justify-content` property determines how flex items are aligned along the main axis of the flex container. It offers several alignment options:

`flex-start`: Flex items are aligned at the start of the container.
`flex-end`: Flex items are aligned at the end of the container.
`center`: Flex items are centered within the container.
`space-between`: Flex items are evenly distributed with space between them.
`space-around`: Flex items are evenly distributed with space around them.

### Align Items

The `align-items` property sets the alignment of flex items along the cross axis of the flex container. It provides the following alignment options:

`flex-start`: Flex items are aligned at the top of the container.
`flex-end`: Flex items are aligned at the bottom of the container.
`center`: Flex items are centered vertically within the container.
`baseline`: Flex items are aligned based on their baselines.
`stretch`: Flex items are stretched to fill the container vertically.

### Flex Wrap

By default, flex items are laid out on a single line. However, if the container's width is not sufficient, flex items can be wrapped onto multiple lines using the `flex-wrap` property. It accepts two values:

- `nowrap`: Flex items are forced to remain on a single line.
- `wrap`: Flex items wrap onto multiple lines as needed.

```css
.container {
  flex-wrap: value;
}
```
### Resources

- [(Article)CSS-Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [(Video)Flexbox crash course](https://www.youtube.com/watch?v=u044iM9xsWU)

## Grid

- [Getting Started](#grid-box-getting-started)
- [Grid Container](#grid-container)
- [Grid Items](#grid-items)
- [Grid Template](#grid-templates)
- [Justify Content](#grid-justify-content)
- [Align Items](#grid-align-items)

### Getting Started

CSS Grid, a powerful layout system that allows us to create flexible and responsive web designs. Grid provides a two-dimensional layout structure, allowing us to define both rows and columns to arrange elements on a webpage.

### Grid Container

The grid container is the parent element that holds all the grid items. By applying the `display: grid` property to an element, we can create a grid container. The grid container allows us to define the overall layout of the grid, including the number of rows and columns.

```css
.container {
  display: grid;
}
```

### Grid Items

Grid items are the child elements of the grid container. They are automatically placed onto the grid based on their order in the HTML markup. You can control their placement using properties like `grid-row` and `grid-column`. Here's an example:

```css
.grid-item {
  grid-row: 1 / 3;
  grid-column: 2 / 4;
}
```

### Grid Template

The grid template is used to define the structure of the grid, specifying the number and size of the rows and columns. We can use keywords such as `auto`, `fr`, and specific lengths to define the dimensions of the grid tracks.

To define a grid template, use the `grid-template-rows` and `grid-template-columns` properties:

```css
.container {
  grid-template-rows: value; /* Two rows with specific heights */
  grid-template-columns: value; /* Two columns with a ratio of for example 1:2 */
}
```
### Code examples

- [Code examples(Grid Container)](https://codesandbox.io/s/grid-container-tkhq72?file=/index.html)
- [Code examples(Grid Items)](https://codesandbox.io/s/grid-items-phxrk2?file=/index.html)
- [Code examples(Grid Template)](https://codesandbox.io/s/grid-template-g2yv4v?file=/index.html)

### Justify Content

The `justify-content` property is used to align the grid items along the horizontal axis (row direction) within the grid container. It controls the distribution of space between and around the grid items.

To justify the content within the grid container, use the following CSS:

```css
.container {
  justify-content: value; /* Align items to the center */
}
```
### Align Items 

The `align-items` property is used to align the grid items along the vertical axis (column direction) within the grid container. It controls the distribution of space between and around the grid items.

To align the items within the grid container, use the following CSS:

```css
.container {
  align-items: value; /* Align items to the center */
}
```

### Resources

- [(Article)CSS-Tricks: A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [(Video)Grid crash course](https://www.youtube.com/watch?v=rg7Fvvl3taU)

# Media Queries

Media queries enable you to apply different styles based on the characteristics of the user's device or browser. They are commonly used for creating responsive designs that adapt to different screen sizes.

## Introduction

Media queries are a powerful feature of CSS that allow you to apply different styles based on the characteristics of the device or browser window. They enable you to create responsive designs that adapt to various screen sizes, resolutions, and orientations. This README.md file provides an overview of media queries, how they work, and why you should use them in your projects.

## How do media queries work?

Media queries consist of a media type and one or more expressions that define the conditions for the styles to be applied. When a media query is encountered, the browser evaluates the conditions and determines whether or not to apply the styles within the media query block.

## Why should you use media queries?

1. **Responsive Web Design**: Media queries are essential for creating responsive web designs that adapt to different devices and screen sizes.
2. **Improved User Experience**: With media queries, you can tailor your content and design based on the device's capabilities, improving readability and usability.
3. **Future-Proofing**: Media queries allow your website to adapt and remain functional across a wide range of devices.

## Mobile-First Approach

In this approach, you design and develop your website primarily for mobile devices and then progressively enhance it for larger screens.

```css
/* Base styles for mobile devices */
body {
  font-size: 16px;
}

/* Media query for tablets */
@media screen and (min-width: 768px) {
  body {
    font-size: 18px;
  }
}

/* Media query for desktops */
@media screen and (min-width: 1024px) {
  body {
    font-size: 20px;
  }
}
```


## Hide/Show Elements

Media queries can also be used to hide or show elements based on screen size.

```css
/* Base styles for all screens */
.container {
  display: block;
}

/* Media query to hide an element on mobile devices */
@media screen and (max-width: 600px) {
  .container {
    display: none;
  }
}
```

# (Optional)Advance Selectors

## Advance Selectors

### Pseudo-classes

**Pseudo-classes**: Selects elements based on a specific state or condition.

```css
/*:hover - selects an element when the mouse pointer is over it: */
button:hover {
  background-color: yellow;
}
```

```css
/* :focus - selects an element when it has keyboard focus: */
input:focus {
  border-color: blue;
}
```

```css
/* :first-child - selects the first child element of its parent: */
ul li:first-child {
  font-weight: bold;
}
```

```css
/* :nth-child() - selects elements based on their position within their parent: */
ul li:nth-child(odd) {
  background-color: lightgray;
}
```

### Code example

- [Pseudo-classes](https://codesandbox.io/s/smoosh-water-37rntk?file=/index.html)

### Child Selector

**Child Selector**: Selects elements that are direct children of another element. It uses a greater than sign (>). For example, `article > p` selects all `<p>` elements that are direct children of a `<article>` element.

```css
article > p {
  /* CSS properties */
  property: value;
}
```

```html
<article>
  <p>This paragraph will be selected</p>
  <div>
    <p>This paragraph will NOT be selected</p>
  </div>
</article>
```

### Adjacent Sibling Selector

Adjacent Sibling Selector: Selects an element that immediately follows another element. It uses a plus sign (+). For example, `h2 + p` selects the `<p>` element that immediately follows an `<h2>` element.


```css
h2 + p {
  /* CSS properties */
  property: value;
}
```

```html
<h2>Title</h2>
<p>This paragraph will be selected</p>
<p>This paragraph will NOT be selected</p>
<h2>Another Title</h2>
<p>This paragraph will be selected</p>
```

### General Sibling Selector

General Sibling Selector: Selects elements that follow another element. It uses a tilde (~). For example, `h2 ~ p` selects all `<p>` elements that follow an `<h2>` element.

```css
h2 ~ p {
  /* CSS properties */
  property: value;
}
```

```html
<h2>Title</h2>
<p>This paragraph will be selected</p>
<p>This paragraph will also be selected</p>
<div>
  <p>This paragraph will be selected</p>
</div>
<h2>Another Title</h2>
<p>This paragraph will be selected</p>
```

### Code example

- [Sibling Selector](https://codesandbox.io/s/sibling-selector-4x8dwc)

### Attribute Selector

Attribute Selector: Selects elements based on their attribute values. It uses square brackets ([]). For example, `[type="text"]` selects all elements with `type="text"` attribute.

```html
<a href="https://example.com">This is a link</a>
<input type="text" placeholder="Enter your name" />
<img src="image.jpg" alt="An image" />
```

```css
a[href="https://example.com"] {
  /* CSS properties */
  property: value;
}
```

```css
input[type="text"] {
  /* CSS properties */
  property: value;
}
```

```css
img[alt="An image"] {
  /* CSS properties */
  property: value;
}
```

### Code example

- [Attribute Selector](https://codesandbox.io/s/attribute-selector-x47lpq)

### More selectors

1. `:active`: Applies styles when an element is being activated, such as when it is clicked and held down.

2. `:disabled`: Applies styles to disabled elements, preventing user interaction.

3. `:enabled`: Applies styles to enabled elements, allowing user interaction.

4. `:checked`: Applies styles to checked radio buttons or checkboxes.

5. `:required`: Applies styles to required form fields.

6. `:optional`: Applies styles to optional form fields.

7. `:valid`: Applies styles to form elements with valid input.

8. `:invalid`: Applies styles to form elements with invalid input.

9. `:last-child`: Applies styles to the last child element of its parent.

10. `:nth-of-type()`: Selects elements based on their position among elements of the same type. It also takes a formula as an argument.

11. `:nth-last-child()`: Selects elements based on their position among the list of siblings, counting from the last child.

12. `:nth-last-of-type()`: Selects elements based on their position among elements of the same type, counting from the last element.

13. `:not()`: Selects elements that do not match a specific selector. For example, `:not(.my-class)` selects elements that do not have the class "my-class".

14. `:root`: The :root selector represents the root element of the document, which is typically the `<html>` element. It is often used to define global CSS variables that can be accessed and reused throughout the stylesheet.

15. `::before` and `::after`: The `:before` and :`after` selectors are used to insert content before or after an element. They are known as pseudo-elements because they create virtual elements that can be styled separately from the actual content of an element.

### Code example

- [More selectors](https://codesandbox.io/s/dreamy-joliot-krgqn4?file=/index.html)
