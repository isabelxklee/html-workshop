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
### Inheritance
Sources:
* [MDN web docs: Cascade and Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)

### Selectors

### Specificity

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

---

## Deliverables
* Import a [google font](https://fonts.google.com) in between the `<head>` tags in `application.html.erb`.

Example:
  ```
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  ```

* In `application.css`, add padding to the `body` element.
* Set the imported google font to be the default font for the whole app.
* Create a header element that persists throughout the whole app.
  * How does this affect the padding that we previously added to the `body` element?
* Style a button and create a hover state and disabled state for it.
* Create a colored background with a rounded border radius on the `/artists` page. Create an unordered list with the artists' names on top of this colored background.