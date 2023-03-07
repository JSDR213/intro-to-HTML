# Introduction To HTML

![html image](https://cdn.lynda.com/course/170427/170427-637363828865101045-16x9.jpg)

## Overview

We'll be going over the basic's of HTML. In this lesson we'll review everything from creating to a HTML file, to building out a full html page.
This lesson covers HTML syntax and element types.

## Objectives

- Learn how to create an HTML file
- Learn about how an HTML file is structured
- Learn about different HTML tags
- Build a simple HTML page


## Getting Started

- Fork and Clone this repository

## What is HTML?

HTML stands for hyper text markup language. It has been in use since the advent of the internet. Every website you visit or interact with is built on or with HTML.

If we think of the human body: Javascript is the Brain and nerves that control our actions. CSS is the skin and hair that define how we look. HTML would be our skeleton that everything is built up on. 


## Creating A HTML File

Inside of this lesson folder, create an `index.html` file. You can either do this in your terminal with `touch index.html` or with vscode's add file button located in your file explorer.

Open the `index.html` file you created. Once the file opens, type `!` and you should see a pop up to use `emmet abbreviations`. Hit the enter key to accept the suggestion. You should be given the following HTML:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

**If emmet did not work for you, feel free to copy and paste the above code into your `index.html`.**


### Stop and Discuss 5 min

Talking points:

- Analyzing the current code
- Why is the file called `index.html`

## HTML Elements

HTML is built with elements or `tags`. For example, the `body` tag is an element. HTML supports many different tags, all of which serve different purposes and uses.


There are probably around 50-100 different HTML elements that exist. The goal of this lesson is not to show you every single HTML tag, but rather to give you examples of some widely used ones, so that as you continue on your journey, you will be able to figure out and use any that you encounter.  


As you can see, elements are wrapped in our angle bracers <> and are closed with a slash </>.
Some require content to be placed within and then closed
```
<h1> I am an H1 tag </h1>
<h2> I am a smaller H2 tag </h2>
```

While others, known as "Void Tags" are simply enclosed within themselves and do not need a second </> to close them off
 

```
<img src="profilePicture.jpg" />
```

The most important rule to understand is that while some elements may be contained within others (known as nesting), they must be closed off before starting a separate set of elements.


This is written correctly, and will work. Don't worry about the content yet, we'll discuss what these elements each do, but focus more on how we are structuring the elements.

```
<div>

    <a href="www.google.com">
      
        <h3> Click here to go to Google! </h3>
      
   </a>

</div>
```


Because our H3 is nested within the Anchor tag (a), it needs to be closed out before the Anchor is. Both of these have to be closed out before the Div is closed.


What is wrong with this block of code here?

```
<div>

  <a href="www.google.com">
  
      <h3> Click here to go to Google 
      
   </a>

      </h3>
      
 </div>      
 ```
 

Hopefully we were able to get our LiveServer extension working yesterday. Click "Go Live!" at the bottom of the VS code screen and watch as your HTML page loads up in your browser! If your LiveServer is not working, let us know, then try to either drag the HTML file into your browser, or right click on the file in VSCode and select "Open With" to open it up in your browser window. You should now see some content on your screen!
 


### Block Elements

Block elements, are `tags` that create a box. These elements stack `vertically` on the page in a column format.

Examples of basic block elements:

| Tag    | Uses                                                                       |
| ------ | -------------------------------------------------------------------------- |
| `div`  | A general use containing element                                           |
| `h<n>` | A header tag used to create different sized headings                       |
| `p`    | A paragraph tag to automatically size text to standard paragraph text size |

#### Semantic Tags

Semantic tags, are elements that have a special meaning. These tags aid screen readers in verbally giving feedback for users with disabilities.
Semantic tags were intoduced in the HTML 5 web standard.

Examples of semantic tags:

| Tag       | Uses                                                                                  |
| --------- | ------------------------------------------------------------------------------------- |
| `nav`     | An element that wraps elements for navigation purposes                                |
| `header`  | This element declares a primary heading section or call to action                     |
| `section` | Containing element to break areas of a page into individual sections                  |
| `article` | Containing element to declare articles on a web page                                  |
| `aside`   | A containing element that is typically used to keep elements to the side on webpages. |

### Inline Elements

These elements are used `inline` of block elements. This means that they stack horizontally and do not break up the flow of a page or element.
They are typically used to join groups of HTML elements on a single line.

Examples of inline elements:

| Tag     | Uses                                                                         |
| ------- | ---------------------------------------------------------------------------- |
| `a`     | Anchor tag used for creating links to external sites or different html pages |
| `span`  | `Spans` mutliple elements into a single line                                 |
| `br`    | Breaks text or elements to a new line on the page                            |
| `input` | An element that accepts a user input                                         |
| `img`   | Used for displaying images on a page                                         |

For a full list of HTML elements visit [W3 Schools](https://www.w3schools.com/html/html_blocks.asp)

  
But thats enough of an intro for now. Lets start writing some code! 

### Adding More Content To Our Page

Head over to your `index.html`. Let's start by adding a nav to our document. Inside of the `nav` tags, add in a `ul` tag followed by 2 `li` tags inside of the `ul`.
The first `li` should contain the text `Home` and the second should contain the text `About`:


A "ul" is an Unordered List. An "ol" will created an numerically ordered list. Nested within these we add our "li" elements, which will be the individual items of the list.

Lets main a main section to our body using the "Main" element, and add a list of things to do

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
  
       <header>
        <h1> I am an H1 tag </h1>
        <h3> I am H3 tag!
       </header>
    
    
        <nav>
          <ul>
            <li>Home</li>
            <li>About</li>
          </ul>
        </nav>
    
    
      <main>
        <h2> Things to do <h3>
          <ol>
            <li> Learn HTML basics </li>
            <li> Practice HTML syntax </li>
            <li> Style our HTML with CSS </li>
          </ol>
       </main>  
        
        
  </body>
</html>
```

Let's preview our changes. 




## Element Attributes

All elements within a HTML document have attributes or properties. These properties allow us to differentiate between elements or asign the same style to multiple elements. (More On This Later)

Here's a list of common html attributes:

| Attribute | Use Case                                                                    |
| --------- | --------------------------------------------------------------------------- |
| `id`      | Used to assign unique id to elements                                        |
| `class`   | Used to give elements the same `name` or `class` to style elements the same |
| `href`    | Used with anchor/`a` tags to define a link for navigation                   |
| `src`     | Used with `img` tags to define a source url for an image                    |

For a full list of HTML attributes visit [W3 Schools](https://www.w3schools.com/html/html_attributes.asp)


Inside of our Main element, but outside of our Ordered List, lets create 2 new boxes in our HTML, and create 3 buttons in each. To create these "Boxes" we are going to use the "Div" element. To make buttons, we simply use the element "Button"!

```
<main> 
    ....


<div>
  <button> Log in </button>
  <button> Create Accounut</button>
  <button> Sign Out </button>

</div>

</main>
```

### Adding Attributes To Our HTML

In your `index.html`, give one div the class of "container", give your "Login" and "Create Account" buttons a class of "login-button", and your Logout button an id of "logout"


```
<div class="container">
  <button class="login-button"> Log in </button>
  <button class="login-button"> Create Account</button>
  <button id="logout"> Sign Out </button>
</div>


```

You will NOT see any changes just yet, we will work with these attributes more in our next lesson on CSS

### You Do 10 min

Add some content to your page! Here are the necessary requirements, but feel free to add your own flair:

- Must have at least 1 `h1` tag.
- Must have at least 1 `p` tag.
- Must have at least 1 `main` tag.
- The `main` must have 2 `div` tags inside of it.
- Give your new div a class of "shopping-container"
- In this Div, add 3 buttons, "Add to Cart", "Continue Shopping", and "Checkout"
- Give all 3 buttons a class of "shopping-buttons", and give the "Checkout" button an ID of "checkout"



## Recap

In this lesson we learned how to set up a HTML file utilizing semantic tags and attributes.
There's more to HTML than meets the eye! Feel free to use this lesson to experiment with the html file and try different element combinations.

## Resources

- [W3 Schools](https://www.w3schools.com/html/default.asp)
- [35+ HTML/CSS Resources](https://medium.com/level-up-web/30-html-css-resources-for-beginners-4e4d0af4b44b)
