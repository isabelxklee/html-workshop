# Rails HTML/CSS Workshop

## What is HTML and CSS?
HTML
* HTML is the standard markup language for creating Web pages and it stands for Hyper Text Markup Language.
* HTML describes the structure of a Web page.

CSS
* Cascading Style Sheets (CSS) is used to format the layout of a webpage. It describes how HTML elements are to be displayed on screen.

## Where to write custom HTML/CSS in your Rails app
* Add any meta data about your website in `app > views > layouts > application.html.erb`
* Write your CSS in `app > assets > stylesheets > application.css`

## What goes in the HTML <head> tag?
* Meta data
* Links to external resources, like stylesheets, imported fonts, favicons, etc.

## HTML meta data
Why is it important to add meta data?
* Accessibility
* SEO

Different types of meta data
* Title:
* Description: 
* Language: 
* Author: 
* Keywords: 
* Favicon: 
* Character set: 

```html
<head>
  <meta charset="UTF-8">
  <meta name="description" content="This is a free HTML/CSS workshop.">
  <meta name="keywords" content="HTML, CSS, coding, programming">
  <meta name="author" content="Isabel K. Lee">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```

## CSS attributes
### Selectors
Element
* Elements are HTML objects that can be styled using CSS.

Class
* A `class` lets you identify multiple elements.

```html
<div class="section">
  <p>Green vines attached to the trunk of the tree had wound themselves toward the top of the canopy. Ants used the vine as their private highway, avoiding all the creases and crags of the bark, to freely move at top speed from top to bottom or bottom to top depending on their current chore.</p>
</div>

<div class="section">
  <p>She wanted rainbow hair. That's what she told the hairdresser. It should be deep rainbow colors, too. She wasn't interested in pastel rainbow hair. She wanted it deep and vibrant so there was no doubt that she had done this on purpose.</p>
</div>
```

```css
div.section {
  background-color: beige;
  color: black;
  font-size: 16px;
}
```

ID
* An `id` can be used to identify a unique HTML element.

```html
<div class="footer">
  <a href="">about me</a>
  <a href="">github</a>
</div>
```

```css
div#footer {
  background-color: black;
  color: white;
}
```

Pseudo-classes and pseudo-elements
* Pseudo-classes allow you to style specific states of an element
* In this example, the `:hover` pseudo-class lets you customize what the `<a>` tag will look like when a cursor is hovering over it.
* `a:hover { }`

Combinators
* Combinators allow us to select `<p>` tag elements that are direct children of `<article>` elements using the child combinator (>).
* `article > p { }`

### Specificity
Specificity is how the browser decides which rule applies if multiple rules have different selectors. It is basically a measure of how specific a selector's selection will be:

An element selector is less specific — it will select all elements of that type that appear on a page — so will get a lower score.

A class selector is more specific — it will select only the elements on a page that have a specific class attribute value — so will get a higher score.

If this is our CSS, which color will the `<h1>` end up being?

```css
#navigation.main-heading { 
  color: red; 
}
        
h1 { 
  color: blue; 
}
```

```html
<h1 class="main-heading" id="navigation">This is my heading.</h1>
```

### Cascade
Stylesheets cascade — at a very simple level this means that the order of CSS rules matter; when two rules apply that have equal specificity the one that comes last in the CSS is the one that will be used.

If this is our CSS, which color will the `<h1>` end up being?

```css
h1 { 
  color: red; 
}
h1 { 
  color: blue; 
}
```

Answer: Since both the CSS rules carry the same specificity, the last one will overrule the other `<h1>` styles above it.

### Inheritance
Inheritance declares that some CSS property values set on parent elements are passed down to their child elements, and some aren't.

For example, if you set a color and font-family on an element, every element inside it will also be styled with that color and font.

However, if you set a width of 50% on an element, all of its descendants do not get a width of 50% of their parent's width.

### Easy to implement CSS themes
* https://watercss.kognise.dev

## Accessibility 101
Color contrast
Alt text
Tabbing through objects
Clear UX copy

## Deliverables
* Import a [google font](https://fonts.google.com) in between the `<head>` tags in `application.html.erb`.

Example:
  ```html
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  ```

* In `application.css`, add padding to the `body` element.
* Set the imported google font to be the default font for the whole app.
* Create a header element that persists throughout the whole app.
  * How does this affect the padding that we previously added to the `body` element?
* Style a button and create a hover state and disabled state for it.
* Create a colored background with a rounded border radius on the `/artists` page. Create an unordered list with the artists' names on top of this colored background.

## Sources and further reading
* [MDN web docs: CSS Building Blocks](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks)
* [MDN web docs: Cascade and Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
* [Sylwia Vargas: CSS-lecture](https://github.com/sylwiavargas/CSS-Lecture-And-Exercises)
* [Sylwia Vargas: Accessible-Web-101](https://github.com/sylwiavargas/Accessible-Web-101)