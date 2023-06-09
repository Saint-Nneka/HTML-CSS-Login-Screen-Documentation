# Creating A Login Screen: Applying Basic Concepts of HTML and CSS

## Introduction

This documentation explores how to create a login screen using HTML and CSS. Focusing on the basic concepts, we will cover page structure in HTML, including the use of semantic HTML tags to structure a web page, the distinction between block and inline elements, and the utilization of tag attributes to identify key information within a page. We will also get to understand how to create HTML text elements including the tags and their attributes afterwhich we introduce CSS to see how it interacts with HTML elemants. Next, we go deeper into understanding the HTML/CSS relationship, siting examples form our login screen. lastly, we will learn some CSS synthax, and apply the knowledge to change the appearance of our login screen.


## Page structure of a login screen in HTML

HTML (Hypertext Markup Language) is the standard markup language used for creating web pages. To create a login screen, we need to first understand how to structure the web page appropriately. This involves using semantic HTML tags, distinguishing between block and inline elements, and utilizing tag attributes to identify key information within the page. <br>

*Semantic HTML tags* provide meaning and structure to the content of a web page. They play a crucial role in improving accessibility, search engine optimization (SEO), and overall code readability by helping these technologies understand the purpose and context of different sections. 
Here are some commonly used semantic HTML tags and their purposes:

`<header>`: Represents the introductory content or a container for navigational elements.
`<nav>`: Defines a section for navigation links.
`<main>`: Indicates the main content of the page.
`<section>`: Defines a section within a document, such as a login form.
`<article>`: Represents a self-contained composition within a document.
`<footer>`: Defines the footer of a document or section.
 
Now, lets see how some of these tags are represented in our login screen:

```html

<body>
  <header>
    <h1>Login</h1>
  </header>

  <main>
    <form>
      <label for="username">Username:</label>
      <input type="text" id="username" name="username" required>

      <label for="password">Password:</label>
      <input type="password" id="password" name="password" required>

      <button type="submit">Log In</button>
    </form>
  </main>

  <footer>
    <p> &copy; 2023 Saint Nneka. All rights reserved.</p>
  </footer>
</body>

```
In this piece of code, we find four semantic HTML tags -header, main, form, and footer- The `<header>` tag represents the top section of the page, containing the login heading. The `<main>` tag signifies the main content area, which includes the login form. The `<form>` tag encapsulates the form elements like inputs and buttons. The `<footer>` tag represents the bottom section of the page, containing copyright information. With is, the structure of our login screen is properly defined.<br>

Another key aspect of HTML page structuring is understanding the concept of *block and inline elements*. These elements have different default behaviors in terms of layout and how they interact with other elements. Block elements typically start on a new line and occupy the full available width, while inline elements don't. They (inline elements) only take up the necessary width to fit their content. Carefully look at these examples from our login screen to appreciate the difference.

```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<button type="submit">Log In</button>
```

Here, `<label>` and `<button>` are block elements, while `<input>` is an inline element. By default, each `<label>` and `<input>` combination will be displayed on a new line due to the block behavior of label.

however, if you place two input elements next to each other as in the example below, they appear on the same line unless you sebarate them with a `<br>` tag.
```html
<label for="password">Password:</label>
<input type="password" id="password" name="password">
```

<!-- Using tag attributes to identify key information within a page:

Tag attributes provide additional information or functionality to HTML elements. They can be used to identify key information within a page, such as form fields or specific labels. Here's an example:

```Html
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<label for="password">Password:</label>
<input type="password" id="password" name="password">

<button type="submit">Log In</button>
```
In this code snippet, the `for` attribute of the <label> element specifies the association between the label and the input field. -->




## Creating HTML Text Elements

a. Recognizing common HTML elements and their corresponding attributes:

Having explained how HTML provide us with various text elements necessary for laying out the structure of our web page, lets expose our mind to some more of these basic HTML elements and also to attributes. Before we go any further, you should know that the function of *HTML attributes* is to provide additional information about an element and allow us to identify key information within a page. That said, let us explore some fundamental elemnts and attributes.

  `<h1> to <h6>`: Heading elements represent different levels of headings, with `<h1>` being the highest level and `<h6>` the lowest. These elements have no specific attributes but are important for structuring content.

```html
<h1> # header 1 </h1>
<h2> # header 2 </h2>
<h3> # header 3 </h3>
<h4> # header 4 </h4>
<h5> # headre 5 </h5>
<h6> # header 6 </h6>

```
`<p>`: The paragraph element represents a paragraph of text. It does not have any specific attributes, but you can style it using CSS.

```html
<p>This is a paragraph of text.</p>
```
`<strong>` and `<em>`: These elements provide emphasis to text. `<strong>` represents strong importance, and is displayed in **bold**, while `<em>` represents emphasized text, typically displayed in *italics*.

```html
<p>Please <strong>login</strong> to continue.</p>
<p>This is <em>very</em> important.</p>
```
`<a>`: The anchor element is used for creating hyperlinks. It requires the `href` attribute, which specifies the destination URL or target location within the current page.

```html
<a href="https://www.example.com">Visit our website</a>
```
`<span>`: You remeber what we said about inline elements? Well, the span element is an inline container used to group and style text or other inline elements. It does not have any specific attributes but can be useful when targeting specific parts of text with CSS or JavaScript.

```html
<p>Please enter your <span class="highlight">username</span> and <span class="highlight">password</span>.</p>
```
These are just a few examples of HTML text elements and their attributes. There are many more elements available to structure and present text-based content. However, lets take an example from our login screen to give a better understanding of the element-attribute interaction.

```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<label for="password">Password:</label>
<input type="password" id="password" name="password">

<button type="submit">Log In</button>
```


In the example, the `<label>` element is used to create labels for the input fields. The`for` attribute specifies the association between the label and the corresponding input field. The `<input>` elements are used to create text input fields. The `type` attribute determines the input field type, such as "text" or "password," while the `id` and `name` attributes provide identification and accessibility to the input fields.

b. Distinguishing between HTML and CSS and identifying their separate uses:
<!-- inset plain HTML image, and then the styled couterpart next to it. -->




## Understanding the HTML and CSS Relationship

HTML and CSS are both essential in web development, and they serve different purposes which we are looking at below.



a. Distinguishing between HTML and CSS and identifying their separate uses:

HTML is used for structuring and defining the content of a web page. It consists of a set of markup tags that describe the elements and their relationships on the page. HTML tags provide the foundation for organizing text, images, forms, links, and other content elements. In the context of our login screen, we used HTML to create the structure and define the text elements such as labels, input fields, and buttons.

Lets take a moment to study our login screen HTML and CSS codebase to inorder to grasp the dynamics.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Login Screen</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>Login</h1>

  <form>
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>

    <button type="submit">Log In</button>
  </form>
</body>
</html>
```
In this HTML code, we have the basic structure of our login screen. The `<head>` section includes a title for the page and a reference to an external CSS file, "styles.css," which contains the CSS rules for styling the login screen. The `<body>` section contains the actual content of the login screen, including the login heading (`<h1>`) and the form elements (`<form>`, `<label>`, `<input>`, and `<button>`).


CSS, which is the stylesheet language controls the visual appearance, layout, and design of HTML elements on a web page. It allows you to define colors, fonts, spacing, positioning, and other visual properties of the HTML elements.

```css
/* styles.css */
<style>
body {
  font-family: Arial, sans-serif;
  background-color: #f1f1f1;
}

h1 {
  color: #333;
}

label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
}

input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 8px;
  margin-bottom: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #4CAF50;
  color: white;
  padding: 10px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
```

In this CSS code, the `<style>` element embeds CSS rules directly within the HTML document. CSS selectors and properties are used to style different elements. For example, we set the font family and background color for the entire body, color for the login heading (h1), formatting properties for labels and input fields, and styling for the login button. These CSS rules modify the appearance of the HTML elements defined in the HTML code without changing the underlying HTML structure. So, by separating the presentation logic using CSS, we can easily modify the appearance of the login screen

The Relationship between HTML and CSS:
HTML and CSS work together to create visually appealing and well-structured web pages. HTML defines the structure and content of the page, while CSS specifies the presentation and styling of those elements.

HTML provides the skeleton and semantic structure of the login screen, using tags to define the different components like headings, forms, labels, and input fields. CSS, on the other hand, adds the visual appeal and enhances the presentation by styling these HTML elements. Combining these two technologies allows us to create an aesthetically pleasing and functional login screen.





## Deeper understanding of CSS:
a. Identifying and using the correct CSS syntax:

CSS (Cascading Style Sheets) uses a specific syntax to apply styles to HTML elements. Understanding and using the correct CSS syntax is crucial when changing the appearance of a login page. Here are some key points for you to note.

CSS styles are defined using selectors, which target specific HTML elements or groups of elements.
Selectors are followed by curly braces `{}` to enclose the style rules.
Style rules consist of a `property` and a `value`, separated by a colon `:`.

Here's an example of CSS syntax:

```css
selector {
  property: value;
}
```

b. Applying CSS to HTML elements:

To change the appearance of a login page using CSS, we target specific HTML elements or classes and apply styles to them. Here's our login screen codebase as example:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Login Page</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>Login</h1>

  <form>
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>

    <button type="submit">Log In</button>
  </form>
</body>
</html>
```

```css
h1 {
  color: #333;
  font-size: 24px;
}

/* Targeting the label elements */
label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
}

/* Targeting the input elements */
input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 8px;
  margin-bottom: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

/* Targeting the button element */
button {
  background-color: #4CAF50;
  color: white;
  padding: 10px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
```

In this example, we have an HTML login page structure, and the CSS code is written in a separate file called "styles.css," which is linked in the HTML `<head>` section.

CSS selectors are used to target specific HTML elements. For example, the selector h1 targets the `<h1>` element, label targets the `<label>` elements, and input[type="text"], input[type="password"] targets the `<input>` elements with the specified type attribute values.

Within the CSS rules, we define various style properties and their corresponding values. For instance, we set the color and font size for the `<h1>` element, display, margin, and font weight for the `<label>` elements, width, padding, and border styles for the `<input>` elements, and background color, padding, and border styles for the `<button>` element.

By applying CSS rules to the HTML elements, we can change their appearance, layout, and behavior, resulting in a customized login page design.

## Conclusion

Now that we know the different roles of HTML and CSS, it behooves us to understand their interactions so we can properly manipulate our web pages to create awesome user interfaces.