---
layout: page
title: Landing Page in 90 Minutes
---

## Tutorial Steps

1. [Introduction to HTML](#introduction-to-html)
2. [HTML Elements](#html-elements)
3. [Let's get coding!](#let's-get-coding)
4. [Diving into CSS](#diving-into-css)
5. [Semantic HTML](#semantic-html)
6. [Extra Points](#extra-points)

-----

## 1.Introduction to HTML

In the first 10 minutes we are going to look at:

* What is HTML?
* What is CSS?
* What is an element?
* How to style an element?

### Goal

By the end of this tutorial you will have built [this webpage.](../../examples/landing_first/index.html "Landing Pages Rule") You can later apply it to be your portfolio, cv or personal project.

-----


#### What does HTML stand for?

**H**yper **T**ext **M**arkup **L**anguage

**HTML** is the language used to build websites. All text and content that you see on the internet is built using HTML.

Try opening any website right now, and try to Inspect it's source, usually by pressing Ctrl+U or Cmd+Alt+U, or just inspecting element if you are in a modern browser.

**CSS** is used with HTML to style the page. We will be learning some of this today but it will also be covered extensively in the next set of tutorials.


## 2.HTML elements

An **element** is an HTML building block. There are paragraphs, headings, links, lists, and [many more.](https://developer.mozilla.org/en/docs/Web/HTML/Element)

HTML elements are made up of an opening tag, followed by content then the closing tag.

```html
<tagname>some content</tagname>
```

Example of a paragraph:

```html
<p>this is a small paragraph</p>
```

Example of a heading:

```html
<h1>This is a big heading</h1>
```

Some HTML elements do not need a closing tag as they are used to place standalone elements on the webpage. For example:

```html
<br>  <!-- A Break, to change line in paragraphs-->
<hr>  <!-- Horizontal ruler -->
<img> <!-- Image -->

<!-- Extra Tip: The elements inside these type of brackets
are comments, and will not appear visible -->

```

To view all the possible tags you can use refer to [W3C Schools HTML Tag List](http://www.w3schools.com/tags/)

-----
## 3.Let's get coding!


### The most important thing about web design

The purpose of design is to present the content. That's it.
Content is the primary element of a website, it should never be last on your list to add after you web designed it.
Written content mostly, is 90% of the Web, however the way we style it will teach us all about the design aspects.

Lets put some content on our blank page:

- Lets give it a title as an <h1>
- Write a paragraph as a <p> (or find some text to be the foundation of your page)
- Let's also add a link to another web-page (since internet is always about connecting you to the next computer on the network)

```html

<h1>My First Step into Web</h1>
<p>Web design encompasses many different skills and disciplines in the production and maintenance of websites. The different areas of web design include web graphic design; interface design; authoring, including standardised code and proprietary software; user experience design; and search engine optimization. Often many individuals will work in teams covering different aspects of the design process, although some designers will cover them all.</p>
<p>The term web design is normally used to describe the design process relating to the front-end (client side) design of a website including writing mark up. Web design partially overlaps web engineering in the broader scope of web development. Web designers are expected to have an awareness of usability and if their role involves creating mark up then they are also expected to be up to date with web accessibility guidelines.</p>
<a href="http://en.wikipedia.org/wiki/Web_Design">More information about Web-Design...</a>
```

Here is an example if you feel lazy, notice how the tags open and close, and also how the heading needs to be closed before opening a paragraph tag.
What would happen if we didn't close the heading tag? Try it out...

Almost 90% of every web page is text, and if you can see it being displayed you are already 90% done,
but it doesn't look pretty at all.

-----

If you don't understand some of the elements, here is a brief run-down.

> #### 🔎 Element: Headings `<h1>`
>
> Headings come in 6 sizes
>
> # `<h1>Heading</h1>`
> ## `<h2>Heading</h2>`
> ### `<h3>Heading</h3>`
> #### `<h4>Heading</h4>`
> ##### `<h5>Heading</h5>`
> ###### `<h6>Heading</h6>`
>
> A `h1` defines the most important heading whereas a `h6` defines the least important.

> #### 🔎 Element: Paragraph `<p>`
>
> Putting content into a `<p>` tag will break your text up into paragraphs. 
> This helps make the content of your page easier to read for the user.
> 
> ```html
> <p>
>   Lorem ipsum is one of those texts you will see very often on people who just started laying out a web-page.
> </p>
> ```

> #### 🔎 Element: Link `<a>`
> A link lets the user click through to another webpage. We use the attribute `href` to indicate where you want the user to go.
> ```html
> <a href="http://en.wikipedia.org/wiki/Web_Design">More information about Web-Design...</a>
> ```

-----

## 4.Diving into CSS

Altough we said we are 90% done, it does not look pretty all, let's get more introduced to CSS.

### Why CSS, and not just HTML?

During the early stages of HTML, quite a lot of extra markup was required to change colors, positioning and other style changes.
It made any page almost impossible to understand.
Rules existed for some elements and people were always getting errors in their html.
This wasn't maintainable. People wanted to separate form and structure from style and appearance.

A proposal was made for externalizing the style into a separate document now simply called CSS to ease up the content writing and it's style formatting

Nowadays, we can bring a piece of text to life with colors, fonts and positioning all around for every specific device by writing rules.

### How CSS Rules Work

In your CSS window, you can try typing

```css
p{ color: blue;}
```

You will see almost instantly, text changing from its black default color to blue. But not the heading or the link, just the paragraph text.

You can read this as:
```css
who{ what: how;}
```

And sometimes you might get the rules confused for trying to change the background color vs the text-color, and plenty of others.
```css
p{
color: blue;
background-color: red;
}
```

You may delete this after you have played around with the colours.

And since our text still needs a lot of rules to be defined, we are going to start from it's main base before going into the finer details. Lets start by giving it some readability.

Positioning is the difference between making something look readable, and pure information overload.

> The `/* some text */` are comments, try writing the rules one by one until you are happy with how the text is positioned.

```css
body{
 /* background-color: pink; */
 /* color: yellow; */
 width: 800px;
 /* margin-left: 100px; */
 /* margin-top: 50px; */
 margin: 0 auto;
 /* font-size: 30px; */
}
```

If you are in CodePen, you won't see the body tag anywhere, but it's essentially all around the code you wrote, there are also some invisible parts like <head> which will define title and other attributes of your HTML document, but we'll discuss these at a later time.

As you can see, width gives our webpage its horizontal space.

Playing with margins will allow you to generate spaces around elements.

Margin: 0 auto is a rule to center it no matter the situation.


Line-height allows us to define how much height we want every paragraph to have, so the text can breathe from top and bottom.

-----

### Fonts & Spacings

In case you feel lost already, [this is how your project should look like](http://codepen.io/knuxus/pen/bwrwOR)

And the main font still could be improved, since readability is our concern let's add another css rule to our body.

```css
body{
/* ... */
line-height: 1.5;
font-family: 'Helvetica', 'Arial', sans-serif;
padding: 4em 1em;
}

h1 {
  margin-top: 1em;
  padding-top: 1em;
}
```

> `em` are the same pixel value of your current font-size, if you haven't set it, it defaults to 16px.

If you have those fonts you will see that it will nicely change the font of all our text and make it look much nicer.

This CSS rules have much more than just one parameter how we are used to before, in this specific case, for people who don't have Helvetica font, will see Arial, if not Arial a default sans-serif font will be applied which even exists in low level systems.

> If you want to experiment with different fonts, and serifed fonts try adding Georgia on top of that list of fonts.

It feels like the layout of this page is already quite readable and fully positioned around its content, but we could add some subtle changes to further improve its readability

-----

### Finding balance in color and contrast

Black text on white background doesn't always cause a great impression, and in greater lenghts can be quite tiring to read over a long period of time.
Usually people try to tone it down by using a shade of grey or other possible faded color to make their text subtle, attractive and less default.

Apply the first commented rule if you want to go to a nicer shade, or the default grey referred as `#555` is usually enough for every eye out there.

```css
body{
  /* ... */
  /* color: #566b78; */
  color: #555;
}

h1 {
  /* ... */
  color: #333;
}

```

Another thing you might notice that our `a` tag is looking blue and not very impressive. Let's make our mark on it and use a string color to call for attention.

Sometimes I don't have to remember all the colors out there or use my color selector tool, many tools like [flatuicolors.com](https://flatuicolors.com/) ease our web design process.

Choose any color which you would like to apply to our link. This will also be your primary color to use throught the site.

```css
a{
  color: #e74c3c;
}
```

This link could be positioned better, and have a much nicer and modern look. Let's use some more css rules that could benefit all your text.

Altough a lot of these sound simple, take a moment to ask your mentor or browse some of them that do not make any sense.

```css

a {
  /* add a border around the link */
  border: 2px solid #e74c3c;
  /* make it rounder */
  border-radius: 20px;
  color: #e74c3c;
  font-size: 0.6em;
  letter-spacing: 0.2em;
  /* make more space for the link */
  padding: 1em 2em;
  /* let the link be all in uppercase */
  text-transform: uppercase;
  /* remove the line under the link */
  text-decoration: none;
  /* these are just a bit advanced for your first css lesson, but don't be dissapointed they make everything look cooler */
  transition: none 200ms ease-out;
  /* but we will transition the color and background in case they change. */
  transition-property: color, background;
}

/* This will only apply to link hover state, usually called a pseudo-selector */
a:hover {
  background: #e74c3c;
  color: white;
}

```

Makes much more sense, right? Remove the comments of this css as soon as you understand the rules of each of those declarations.

-----
### Adding more identity

Since the web has evolved, people are not only limited to the basic system fonts or simple colors, we have tools like Google Fonts, and a few others that can virtually bring any type into the web.

Visit [Google Fonts](https://fonts.google.com/) and choose a font that would work for your page.

If you feeling undecisive, choose a sans-serif font. If that still doesn't help, choose Roboto, Open Sans or Lato.

Different fonts will make subtle changes to the general feel of the website, sometimes you need to be more serious, sometimes more playful. Let's go with Roboto for our website.

Pressing the plus icon on the font you can see it in a small popup drawer and using the `@import` method you can copy paste that entire line inside your CSS area, on top of everything like this:

And don't forget to change our font-family declaration to include it as the first font.

```css
@import 'https://fonts.googleapis.com/css?family=Roboto';

body{
  /* ... */
  font-family: 'Roboto', 'Helvetica', 'Arial', sans-serif;
}
```

Try to take a moment to appreciate how nice and simple this look, but also how much code have you already learned to make this.

-----
### An < img > is worth a thousand words


So far we’ve learned about how to add text, headings and links to our page. Now let’s add some images! If we are doing this on your computer, we’ll need to add the image files we want to use to the project folder. If you are still on CodePen, skip the next line. 

It’s good practice to keep images in their own folder, so first, create a folder called ‘images’ inside the same folder as your index.html file. 

Next, download the images you’ll need. Do this by right clicking on the following link, select ‘Save Link As…’, and save it to the images folder you just created.

> We would usually recommend going for a higher quality image, that you either have taken in the past, or using sources like [Unsplash](https://unsplash.com/).

Choose anything that you like, since this is a web design site we will go with [this one.](https://hd.unsplash.com/photo-1468070454955-c5b6932bd08d)

Let's first add it to our HTML, just to see how it looks, and later move it around where it really matters.

Here is a brief explanation how the element works.

> #### 🔎 Element: Image `<img>`
>
> Images are primarily made up of three attributes
> 
> * the `<img>` tag
> * the `src` attribute, which lets the page know what image we want to view
> * the `alt` attribute, this provides extra information if the image cannot be seen on the webpage for any reason
>

In order for us to see this image on the webpage we need to link to the image, this involves telling the webpage where it is and what it is called. Before the main heading of the page, add the following

```html
  <img src="https://hd.unsplash.com/photo-1468070454955-c5b6932bd08d" alt="codeatuni.com">
```

Here you can see we have told the `src` of the image to look in either a file or a url, then we have given it a relevant `alt` attribute.

If you think its too big, try applying some css to it like this:

```css
img{
  width: 100%;
  height: auto;
}
```
-----
## 5.Semantic HTML

Before we proceed we have to get better at naming things.

Let's call the first section of our heading and image a header, and everything else main section.
> #### 📘 Extra Notes: ####
> It has become increasingly important in HTML to make it more readable by not just humans but robots as well; you probably know this as Search Engine Optimisation (or SEO)
>
> For instance, footers, sidebars and headers are not usually the main reason people go to websites so when Google's army of web crawler robots index those, they focus on reading the parts you defined as content and ignore the finer details in footers or sidebars.
>
> There is a whole industry dedicated to making your website more Google friendly and this is the basis of what they do.


Let's wrap up our existing code in two sections, and even add a third one, calling it footer.

```html
    <header>
        <img src="https://hd.unsplash.com/photo-1468070454955-c5b6932bd08d" alt="codeatuni.io">
        <h1>My First Step into Web</h1>
        <a href="http://en.wikipedia.org/wiki/Web_Design">About Web-Design</a>
    </header>
    <main>
        <p>
          Web design encompasses many different skills and disciplines in the production and maintenance of websites. The different areas of web design include web graphic design; interface design; authoring, including standardised code and proprietary software; ser experience design; and search engine optimization. Often many individuals will work in teams covering different aspects of the design process, although some designers will cover them all.
        </p>
        <p>
          The term web design is normally used to describe the design process relating to the front-end (client side) design of a website including writing mark up. Web design partially overlaps web engineering in the broader scope of web development. Web designers are expected to have an awareness of usability and if their role involves creating mark up then they are also expected to be up to date with web accessibility guidelines.
        </p>
        <!-- <a href="http://en.wikipedia.org/wiki/Web_Design">More information about Web-Design...</a> -->
        <br>
    </main>
    <footer>
        <p>&copy; My Awesome First Website - Developed with help of CodeAtUni</p>
    </footer>
```

Let's also add some css regarding our new footer section.

```css
footer{
  text-align: center;
  font-size: 0.7em;
  color: #ddd;
}
```

If you feel lost here is how [it should look like.](http://codepen.io/knuxus/pen/ZpoBwY?editors=1100)

-----

### 6.Modern, big hero images

That re-arrangement of elements happened for a reason, not only google is more able to read our site, but also we can now apply some beatiful full-width imagery on it, like the current modern trend of websites use. If you see AirBnB, Paypal, etc.. they all have a big image on the background, text on top... as you start coding more and more you will notice a lot of trends like that one.

So let's be trendy. Remove our `<img>` element but keep its src value and call it a background image to our header attribute in css.

``` css
header{
  background-image: url('https://hd.unsplash.com/photo-1468070454955-c5b6932bd08d')
}
```

Not pretty at all, we will have to move some more CSS classes around until we get the desired effect.

Remove the width and margin and padding from body, and move it to a new declaration of the `<main>` element, all this inside your css.

```css
main{
  width: 800px;
  margin: 0 auto;
  padding: 4em 1em;
}
```

Black text never looks good on this background, so lets change it to white. But since we have already defined one of the colors for headings we need to redefine it more specifically.
```css
header h1{
  color: #fff
}
```

By telling `header h1` we are saying all the `<h1>` elements inside of our `<header>` element, this will be necessary for every next declaration out there.

You may notice that we are still having some margins on every side of the page, we need to apply a simple rule to our body to prevent those margins from appearing.

This process is called in the industry a CSS Reset. We will just touch the necessary bit of it here, by adding to our body css declaration the value of margin: 0.

```css
body{
  margin: 0;
  /* ... */
}
```

-----

## 7.Extra Points

### Twitter share

Add a share on twitter link along with your other sharing links.

```html
<a href="http://twitter.com/home?status=I love coding HTML! via @codeatuni">Share your love of coding on twitter</a>
```

-----


## Adding a Sidebar

Most of the time in HTML and CSS you will be wondering how to position one content next to another. 

You can always try to float content, left or right with css, but usually that will also throw your text all over the place and get you nowhere.

There are a lot of frameworks like Bootstrap, that give you the power of using a grid system in web design. For you to put one element on one row, or two elements in the same row, usually by telling how many columns does it have.

Altough we're not going to use Bootstrap here we will be using the same concept of rows and columns to create a sidebar next to our main piece of content.

Let's wrap our content within a div, with a class row and put an extra element after our main, called aside, just like this:

```html
    <header>
        <!-- our header -->
    </header>
    <div class="row">
      <main>
          <!-- our main content -->
      </main>
      <aside>
        <!-- New content will come here -->
      </aside>
    </div>
    <footer>
        <!-- our footer content -->
    </footer>
```

If we put some more text into our new aside element you will see it does not look pretty at all, and it will try to find its own space within the rules we defined earlier.

Here is an example content for your aside, `<ul>` stands for unordered list, `<li>` for list item, and the rest you already know.

```html
  <aside>
     <h3> My Favorite Links</h3>
     <ul>
         <li>
             <a href="http://codeatuni.com">Code at Uni</a>
         </li>
         <li>
             <a href="http://codeacademy.com">Codeacademy</a>
         </li>
         <li>
             <a href="http://wikipedia.com">Wikipedia</a>
         </li>
         <li>
             <a href="http://youtube.com">Youtube</a>
         </li>
     </ul>
  </aside>
```

Let's go back to CSS and get that row logic sorted.

First, we need to re-order our `main` rules to apply to our newly created `.row`

```css

/* this was our previous main */
.row{
  max-width: 50rem;
  margin: 0 auto;
  padding: 4em 0;
}

/* our new main has to be smaller to fit the sidebar */
main{
 max-width: 70%;
 float: left;
}

/* both of elements main and aside need to be aligned to the left,
 which in css we call float */
aside{
  padding: 1em 2em;
  float: left;
}
```

Altough you can now see that our main and sidebar are on the same line, and each has its own space, we see that footer has also gone out of place.

To fix this, and usually all the other problems coming from using `float` we need to clear those floats with a css rule called `clear:both`

If we add it to our footer, it will look something like this:

```css
footer{
  clear: both;
  text-align: center;
  padding: 2em;
  font-size: 0.7em;
  color: #ddd;
}
```

And now our footer is back in its previous place, looking even better than before.

-----


### Making first link in our Sidebar different

Some selectors can be so specific in the css that we can style out only the first element, the last, and even much more

In our sidebar, if we wanted to say that our first link needs to be different, we could apply the pseudo selector, `:first-child` to our list like this:

```css

li:first-child a{
  color: #509bee;
  font-size: 21px;
  font-weight: bolder;
}
```

There is a lot more of pseudo selectors, that you can see in our example page if you Inspect the other elmenets, try to find them and apply them to your own code.

-----

This ends our first lesson, we hope you enjoyed it and learnt something.
If you have some spare time how about going back through this tutorial and, by yourself,
make some amendments.

If there is something you did not understand or want to give us some feedback,
 please [send us an email.](mailto:feedback@codeatuni.io) or come and chat on our slack!

## Further reading

* [HTML elements](https://developer.mozilla.org/en/docs/Web/HTML/Element)

-----

## Weekend Coding Course on your campus

- Full course on HTML, CSS, and Javascript for beginners.
- 12 hours of instruction led by professional instructors
- This accelerated course ensures you'll learn to code in just one weekend.
- You will have built your own custom website by the end of the weekend.
- Application required and, if you are accepted, course fee is required [£159]. Applications are competitive.
- Free lunch on both days and chance to meet other tech focused students.

### APPLICATIONS ARE NOW OPEN - LEARN MORE AND APPLY AT: [www.codeatuni.com](http://www.codeatuni.com/)

We will accept applicants on the quality of their application, but don't worry: this course is entirely for BEGINNERS - no coding knowledge required!

[Like us on Facebook](https://www.facebook.com/CodeatUni1) to stay up to date

-----
