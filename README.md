# Rails HTML/CSS Workshop

## What is HTML and CSS?

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

## CSS attributes
### Selectors

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
* 

Alt text
* 

Tabbing through objects
* 

Clear UX copy
* 

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