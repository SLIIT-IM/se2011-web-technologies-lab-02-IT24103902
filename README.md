# SE2011---Web-Technologies---Lab-02
# Lab Sheet 02 – CSS Styling for the Website

**Module:** IT1100 – Internet and Web Technologies  
**Topic:** CSS Basics and Page Styling  
**Duration:** 2 Hours  
**Type:** Self-guided lab sheet  
**Important:** This lab sheet continues from **Lab Sheet 01 – HTML Website Skeleton**. You must use the same website you created in Lab 01 and apply all CSS changes to that existing project.

---

## 1. Learning outcomes

By the end of this lab, you should be able to:

- understand what CSS is and why it is used
- identify the three ways of using CSS:
  - inline CSS
  - internal CSS
  - external CSS
- practice inline CSS, internal CSS, and external CSS
- create and connect an external CSS file
- apply CSS to an existing HTML page
- style headings, paragraphs, images, navigation bars, tables, forms, and footer
- use selectors such as element selectors, class selectors, and ID selectors
- improve the appearance of the website created in Lab 01
- continue the same website so it is ready for the JavaScript lab

---

## 2. What you will do in this lab

In Lab 01, you created the **structure** of the website using HTML.

In this lab, you will style that same website using CSS so that it becomes a clean, simple, nice-looking page.

You will:

- keep the same `index.html`
- learn the three ways of applying CSS
- practice **inline CSS**
- practice **internal CSS**
- create a CSS file named `styles.css`
- link that CSS file to `index.html`
- style the website step by step using **external CSS**
- apply the final task on top of the **final answer from Lab 01**

So this lab is not a new website.  
It is the **same Campus Tech Store website**, improved using CSS.

---

## 3. Before you start: what is CSS?

CSS stands for **Cascading Style Sheets**.

CSS is used to control how HTML elements look on the page.  
For example, CSS is used for:

- colors
- fonts
- spacing
- borders
- alignment
- layout
- hover effects

CSS can be written in three ways:

- **inline CSS**
- **internal CSS**
- **external CSS**

In this lab, you will learn all three.  
However, for a complete website, **external CSS** is the best and most organized method.

---

## 4. The three ways of using CSS

Before styling the full website, let us understand the three methods.

### 4.1 Inline CSS

Inline CSS is written **inside an HTML tag** using the `style` attribute.

### Example:

```html
<p style="color: blue;">This is a blue paragraph.</p>

```

### Why is it called inline CSS?

Because the CSS is written directly **in the same line** or inside the HTML element itself.

### When is it useful?

Inline CSS is useful for:

- very small quick changes
- testing a style quickly
- styling only one single element

### What is the disadvantage?

It is not a good choice for large websites, because:

- it mixes HTML and CSS together
- it becomes hard to manage
- you must repeat code many times

---

### 4.2 Internal CSS

Internal CSS is written inside the `<style>` tag in the `<head>` section of the HTML file.

### Example:

```html
<head>
    <style>
        p {
            color: green;
        }
    </style>
</head>

```

### Why is it called internal CSS?

Because the CSS stays **inside the same HTML file**.

### When is it useful?

Internal CSS is useful for:

- styling one single page
- testing styles while learning
- small projects with only one page

### What is the disadvantage?

It is not ideal for bigger websites, because:

- all styles stay inside one HTML file
- if you have many pages, you must repeat the same CSS in each file

---

### 4.3 External CSS

External CSS is written in a **separate `.css` file** and linked to the HTML file.

### Example in HTML:

```html
<link rel="stylesheet" href="styles/styles.css">

```

### Why is it called external CSS?

Because the CSS is stored **outside the HTML file**.

### Why is it the best method for this lab?

Because it:

- keeps HTML and CSS separate
- makes the code cleaner
- makes changes easier
- can style many pages from one file

---

## 5. Quick practice – inline CSS

Before moving to the full website styling, let us practice inline CSS.

Open your `index.html` file and temporarily try this small example inside the `<body>`:

### Example:

```html
<h2 style="color: darkred;">Inline CSS Example</h2>
<p style="background-color: lightyellow;">This paragraph uses inline CSS.</p>


```

### Explanation

### `style="color: darkred;"`

This directly changes the text color of the heading.

### `style="background-color: lightyellow;"`

This directly changes the background color of the paragraph.

### Practice task

Try changing:

- the heading color
- the paragraph background color
- the text alignment

### Example:

```html
<p style="color: white; background-color: teal; text-align: center;">
    Practicing inline CSS is simple.
</p>


```
### Important note

After practicing, you may remove these examples or keep them only for learning.  
For the main website styling, we will mainly use **external CSS**.

---

## 6. Quick practice – internal CSS

Now let us practice internal CSS.

Inside the `<head>` section of `index.html`, temporarily add:

### Example:

```html
<style>
    .internal-demo {
        color: white;
        background-color: darkblue;
        padding: 10px;
    }
</style>

```
Now inside the `<body>`, add:

### HTML:

```html
<p class="internal-demo">This paragraph uses internal CSS.</p>


```

### Explanation

### `<style> ... </style>`

This is where internal CSS is written.

### `.internal-demo`

This is a class selector.

It styles any element with:

```html
class="internal-demo"

```
### `padding: 10px;`

This adds space inside the paragraph.

### Practice task

Try changing:

- the background color
- the text color
- the font size

### Example:

```html
<style>
    .internal-demo {
        color: black;
        background-color: lightgreen;
        font-size: 20px;
        padding: 10px;
    }
</style>

```
### Important note

Internal CSS is useful for learning, but for the full website, we will now move to **external CSS**.

---

## 7. Project folder you should already have

You should already have this folder structure from Lab 01:

```text
IWT_Lab_01
│
├── src
│   ├── images
│   │   ├── logo.png
│   │   └── hero.jpg
│   ├── styles
│   ├── js
│   └── index.html


```
Now, for this CSS lab, create this new file inside the `styles` folder:

```text
IWT_Lab_01/src/styles/styles.css

```

## 8. Step 1 – Create the CSS file

Inside the `styles` folder, create a file named:

```text
styles.css

```

Path:

```text
IWT_Lab_01/src/styles/styles.css

```
## 9. Step 2 – Link the CSS file to `index.html`

Open your existing `index.html` from Lab 01.

Inside the `<head>` section, add this line:

```html
<link rel="stylesheet" href="styles/styles.css">

```
So your `<head>` section should now look like this:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Campus Tech Store</title>

    <!-- Internal CSS practice -->
    <style>
        .internal-demo {
            color: white;
            background-color: darkblue;
            padding: 10px;
        }
    </style>

    <!-- External CSS file -->
    <link rel="stylesheet" href="styles/styles.css">
</head>


```

### Explanation

### `rel="stylesheet"`

This tells the browser that the linked file is a stylesheet.

### Why do we add it?

Because the browser must know that this file contains CSS rules.

### `href="styles/styles.css"`

This gives the file path to the CSS file.

### Why do we add it?

Because the browser needs to know where the CSS file is located.

### Why do we still keep the `<style>` section here?

Because students need to learn and practice **internal CSS** too.

### Important

In this lab:

- **inline CSS** is practiced directly inside an element
- **internal CSS** is practiced inside `<style>`
- **external CSS** is used for the main full website styling

---

## 10. Step 3 – Update the HTML slightly so CSS can target it better

Before writing CSS, make these small improvements to your Lab 01 final HTML.

### 10.1 Add a class to the logo image

Change this:

```html
<img src="images/logo.png" alt="Campus Tech Store Logo" width="120">


```
to this:

### HTML:

```html
<img src="images/logo.png" alt="Campus Tech Store Logo" width="120" class="logo">

```

to this:

### HTML:

```html
<img src="images/logo.png" alt="Campus Tech Store Logo" width="120" class="logo">


```

### Why do we add `class="logo"`?

Because a class helps us target this image in CSS and style it separately.

---

### 10.2 Add a class to the products table

Change this:

### HTML:

```html
<table border="1">

```

to this:

### HTML:

```html
<table class="product-table">

```

### Why do we remove `border="1"`?

Because now the table border should be controlled by CSS, not by HTML.

### Why do we add `class="product-table"`?

Because we want to style this table in a clean and organized way from CSS.

---

### 10.3 Add a class to the contact form

Change this:

### HTML:

```html
<form>


```

### Why do we add this class?

Because later we will style the form area, input boxes, and button more easily.

---

### 10.4 Wrap the content inside a container

Inside the `<body>`, place all visible content inside a wrapper `<div>`.

So change your body from this style:

### HTML:

```html
<body>
    ...
</body>


```
to this:

### HTML:

```html
<body>
    <div class="container">

        <!-- all your existing content goes here -->

    </div>
</body>


```

### Why do we add a container?

Because a container helps keep the page centered and gives the whole website a neat width.

---

## 11. Step 4 – Start writing CSS

Now open `styles.css`.

We will build the styling in small steps.

---

## 12. Step 5 – Add basic page styling

Type this into `styles.css`:

### CSS:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f6f8;
    color: #222222;
    margin: 0;
    padding: 0;
}

.container {
    width: 85%;
    margin: auto;
    background-color: #ffffff;
    padding: 20px;
}


```

### Explanation

### `body`

This selector targets the whole page.

### `font-family: Arial, sans-serif;`

This changes the text style.

### `background-color: #f4f6f8;`

This gives the page a light background color.

### `color: #222222;`

This sets the default text color.

### `margin: 0;`

Browsers add default space around the page, so we remove it.

### `.container`

This selector targets any element with class `container`.

### `width: 85%;`

This makes the content area take 85% of the page width.

### `margin: auto;`

This centers the container horizontally.

---

## 13. Step 6 – Style the header

Add this below the previous CSS:

### CSS:

```css
header {
    text-align: center;
    padding: 20px 0;
    background-color: #e8f1fb;
    border-bottom: 2px solid #c7d8ea;
}

.logo {
    display: block;
    margin: 0 auto 10px auto;
}

header h1 {
    margin: 10px 0 5px 0;
    color: #1d4d7a;
}

header p {
    margin: 0;
    font-size: 18px;
}


```

### Explanation

### `text-align: center;`

This centers the header text.

### `padding: 20px 0;`

This adds space inside the header.

### `border-bottom`

This adds a line under the header.

### `.logo`

This styles the image with class `logo`.

### `display: block;`

Images are inline by default. We change it so it can be centered more easily.

### `margin: 0 auto 10px auto;`

This centers the image and adds bottom space.

---

## 14. Step 7 – Style the navigation menu

Add this CSS:

### CSS:

```css
nav {
    background-color: #1d4d7a;
    margin-top: 15px;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    text-align: center;
}

nav ul li {
    display: inline-block;
}

nav ul li a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 14px 20px;
}

nav ul li a:hover {
    background-color: #163a5b;
}


```

### Explanation

### `list-style-type: none;`

This removes bullet points from the list.

### `display: inline-block;`

This makes the list items appear next to each other.

### `text-decoration: none;`

This removes the default underline from links.

### `:hover`

This changes the style when the mouse is placed over the link.

---

## 15. Step 8 – Style the sections

Add:

### CSS:

```css
section {
    padding: 25px 0;
    border-bottom: 1px solid #dddddd;
}

section h2 {
    color: #1d4d7a;
    margin-bottom: 10px;
}

section p {
    line-height: 1.6;
}



```

### Explanation

### `section`

This styles all section elements.

### `line-height: 1.6;`

This increases the space between lines and makes text easier to read.

---

## 16. Step 9 – Style the hero image

Add:

### CSS:

```css
#home img {
    display: block;
    margin: 20px auto;
    max-width: 100%;
    border-radius: 8px;
}


```

### Explanation

### `#home img`

This targets the image inside the element with `id="home"`.

### `max-width: 100%;`

This prevents the image from overflowing outside the content area.

### `border-radius: 8px;`

This rounds the corners.

---

## 17. Step 10 – Style the products table

Add:

### CSS:

```css
.product-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
}

.product-table th,
.product-table td {
    border: 1px solid #b7c7d6;
    padding: 12px;
    text-align: left;
}

.product-table th {
    background-color: #1d4d7a;
    color: white;
}

.product-table tr:nth-child(even) {
    background-color: #f2f7fb;
}


```

### Explanation

### `width: 100%;`

This makes the table stretch to the width of the container.

### `border-collapse: collapse;`

This makes table borders join together.

### `padding: 12px;`

This gives space inside each cell.

### `tr:nth-child(even)`

This selects even rows.

---

## 18. Step 11 – Style the ordered list in the Student Offers section

Remember: in Lab 01 final task, students added a **Student Offers** section.  
Now we will style that too.

Add:

### CSS:

```css
#offers ol {
    padding-left: 20px;
}

#offers li {
    margin-bottom: 8px;
}



```

### Explanation

### `padding-left: 20px;`

This gives proper left spacing for the list numbers.

### `margin-bottom: 8px;`

This gives vertical spacing between list items.

---

## 19. Step 12 – Style the contact form

Add:

### CSS:

```css
.contact-form {
    background-color: #f8fbfd;
    padding: 20px;
    border: 1px solid #d3e0ea;
    border-radius: 8px;
}

.contact-form label {
    font-weight: bold;
}

.contact-form input[type="text"],
.contact-form input[type="email"],
.contact-form textarea {
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    margin-bottom: 15px;
    border: 1px solid #bbbbbb;
    border-radius: 4px;
    box-sizing: border-box;
}

.contact-form input[type="submit"] {
    background-color: #1d4d7a;
    color: white;
    border: none;
    padding: 12px 20px;
    cursor: pointer;
    border-radius: 4px;
}

.contact-form input[type="submit"]:hover {
    background-color: #163a5b;
}



```

### Explanation

### `input[type="text"]`

This targets text input fields.

### `textarea`

This styles the message box.

### `width: 100%`

This makes the field take the full width of the form.

### `box-sizing: border-box`

This makes width calculation easier.

### `cursor: pointer`

This changes the mouse cursor on the button.

---

## 20. Step 13 – Style the footer

Add:

### CSS:

```css
footer {
    text-align: center;
    padding: 20px 0 10px 0;
    color: #555555;
    font-style: italic;
}

footer hr {
    border: 0;
    border-top: 1px solid #000000;
    margin-bottom: 15px;
}

footer a {
    color: #1d4d7a;
    text-decoration: none;
}

footer a:hover {
    text-decoration: underline;
}


```

## 23. Check your work

After saving both files, open `index.html` in the browser and check these:

- the page has a light background
- the content appears inside a centered white area
- the header looks neat
- the menu is horizontal
- the table looks styled
- the Student Offers list is readable
- the form fields are full width and neat
- the footer is centered and styled
- the inline CSS example is visible
- the internal CSS example is visible
- the external CSS styles are visible

---

## 24. Common mistakes and fixes

### Problem: CSS is not applying

Check:

- did you create `styles.css` inside the `styles` folder?
- did you write this correctly in the HTML?

### HTML:

```html
<link rel="stylesheet" href="styles/styles.css">


```

- did you save both files?

### Problem: Internal CSS is not working

Check:

- did you place the `<style>` section inside `<head>`?
- did you use the class name correctly?

### Problem: Inline CSS is not working

Check:

- did you write the `style` attribute inside the HTML tag?
- did you use correct CSS property names?

### Problem: The menu is still vertical

Check:

- are you styling `nav ul li` with `display: inline-block;`?
- did your HTML keep the `<ul>` and `<li>` structure?

### Problem: The table still looks old

Check:

- did you remove `border="1"` from the table?
- did you add `class="product-table"`?

### Problem: The logo is not centered

Check:

- did you add `class="logo"` to the image?
- did you include `.logo` CSS?

---

## 25. Final task for the second hour

This final task must be done using the **website that already includes the Lab 01 final task answer**.

That means you must continue from the version that already has:

- Student Offers section
- USB Flash Drive product
- Phone Number input
- W3Schools footer link

Now, apply these extra CSS improvements to that same website.

You must also practice all three CSS methods in this final task:

- inline CSS
- internal CSS
- external CSS

---

## Final Task – Improve the styling further

### Task A – Practice inline CSS

Using **inline CSS**, style one sentence in the Home section.

Requirements:

- change the text color
- make the text bold

### Example:

```html
<p style="color: darkgreen; font-weight: bold;">
    This sentence is styled using inline CSS.
</p>



```

### Task B – Practice internal CSS

Using **internal CSS**, add a style for a small note in the About section.

Inside `<head>`, add or edit the `<style>` section like this:

### HTML:

```html
<style>
    .about-note {
        background-color: #eef7ff;
        color: #003366;
        padding: 10px;
        border-left: 4px solid #3399cc;
    }
</style>


```

Then inside the About section, add:

### HTML:

```html
<p class="about-note">This note is styled using internal CSS.</p>


```

### Task C – Highlight the Student Offers section using external CSS

Style the `#offers` section so that it stands out from the other sections.

Add:

- a light yellow background
- a left border
- some extra padding

---

### Task D – Make the product table rows react on hover using external CSS

When the user moves the mouse over a product row, change its background color.

---

### Task E – Style the phone number field exactly like the other input fields using external CSS

Make sure it is included in the CSS selector and gets the same width, padding, and border styling.

---

### Task F – Improve the footer link using external CSS

Make the external link bold, and add a different color on hover.

---


## 27. Explanation of the final task

### Why do we include all three CSS methods?

Because students should not only know the names of the three methods.  
They should also practice each one.

### Why is external CSS still the main method?

Because it is the best method for styling a full website in a clean and organized way.

### Why is this final task useful?

Because it helps students practice:

- inline CSS
- internal CSS
- external CSS
- styling sections
- styling tables
- styling forms
- styling links

---

## 28. What happens in the next lab

In the next lab sheet, you will continue with this same HTML + CSS website and add **JavaScript**.

You will use JavaScript to add simple interactive features such as button actions, dynamic text changes, and other page behavior.

---

## 29. What to upload to GitHub

Upload the updated project with:

- `index.html`
- `styles/styles.css`
- image files
- the completed final task changes

Your project should now look like this:

```text
IWT_Lab_01
│
├── src
│   ├── images
│   │   ├── logo.png
│   │   └── hero.jpg
│   ├── styles
│   │   └── styles.css
│   ├── js
│   └── index.html

```

## 30. Submission reminder

Before submission, make sure:

- your HTML file works
- the CSS file is connected properly
- the images are included
- inline CSS practice is included
- internal CSS practice is included
- external CSS styling is included
- the final task is completed
- the file names are correct
- the project is uploaded to GitHub properly

---

---

<div align="center">

<svg width="100%" height="90" viewBox="0 0 800 90" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Decorative divider">
  <defs>
    <linearGradient id="lineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#dbeafe"/>
      <stop offset="50%" stop-color="#60a5fa"/>
      <stop offset="100%" stop-color="#dbeafe"/>
    </linearGradient>
  </defs>
  <line x1="80" y1="45" x2="320" y2="45" stroke="url(#lineGrad)" stroke-width="3"/>
  <circle cx="400" cy="45" r="10" fill="#60a5fa"/>
  <circle cx="400" cy="45" r="4" fill="#ffffff"/>
  <line x1="480" y1="45" x2="720" y2="45" stroke="url(#lineGrad)" stroke-width="3"/>
</svg>

# Final Note

Well done on reaching the end of this CSS lab sheet.

You have taken another important step in learning how to build and style web pages.  
Keep practicing each part carefully, try small changes on your own, and continue improving your work step by step.

Wishing you all the best with the rest of the lab activities.

**Happy coding.**

</div>



