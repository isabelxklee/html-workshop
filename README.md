# Rails HTML/CSS Workshop

## What is HTML and CSS?

## Writing custom HTML/CSS to your Rails app
* Add any meta data about your website in `app > views > layouts > application.html.erb`
* Write your CSS in `app > assets > stylesheets > application.css`

## Adding HTML meta data
* title:
* description: 
* favicon: 
* external links/dependencies: 

## CSS attributes
#### Inheritance
Sources:
* [MDN web docs: Cascade and Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)

#### Selectors

#### Specificity

#### Easy to implement CSS themes
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
* Style a button and create a hover state and disabled state for it.
* Create a header element that persists throughout the whole app.