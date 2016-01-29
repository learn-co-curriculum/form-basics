# Form Basics

## Objectives

1. Learn what a form tag is and how to use it
2. Understand how to use the "method" and "action" attributes. 

## Overview

Have you ever posted on someone's Facebook wall? Tweeted about a recent event? How about made a search on Google? Then you've filled out an HTML form. Forms are how we are able to take input from our users through the web. Today, we'll be looking at the basic structure of an HTML form tag. 

## Lesson

An HTML form consists of an opening and closing `form` tag. Inside of the `form` tags are any number of `input` tags. The `form` tag is like the envelope - it wraps around some content and determines the location to which it will be sent.

```html
<form>
</form>
```
Two important attributes of a `form` are the `method` and `action`. The `method` refers to the type of HTTP request that will be made when the form is submitted. The `action` refers to the route where we'll be making the request. The form below will make a 'POST' request to the '/form_submission' route of our application. 

```html
<form method="post" action="/form_submission">
</form>
```

The code above won't actually display anything on our web page. This is because our form has no inputs. Inside of the opening and closing `form` tags, we can add as many inputs as we like. Like the `img` element, our `input` elements are "self-closing" tags. 

```html
<form method="post" action="/form_submission">
	<input>
</form>
```

One important attributes of an `input` tag is the  `type`. This describes what type of data we're expecting to receive, such as `text`, `email`, or `password`. For example, if we choose `password`, the text a user types won't be displayed on their screen.  

```html
<form method="post" action="/form_submission">
	<input type="text">
	<input type="password">
</form>
```

Another important attribute of our input is the `name`. The `name` attribute will act as a label on our server - it's how we can access that value on our server.

```html
<form method="post" action="/form_submission">
	<input type="text" name="username">
	<input type="password" name="password>
</form>
```

Let's also add a submit button so our users can submit the form. We can use an input with the type of "submit." 

```html
<form method="post" action="/form_submission">
	<input type="text" name="username">
	<input type="password" name="password>
	<input type="submit">
</form>
```

Other useful attributes of inputs are `value` and `placeholder`. Value will pre-fill in our inputs with whatever value we choose. This is useful if we want our form to have some default that our user can edit. Placeholder, on the other hand, doesn't actually fill out the form, just lightly displays some text on the input. 

We can also label our inputs using the `label` tag - this simply tells our user which input they are filling out. We can associate a label with an input by adding an `id` attribute to our input. 

```html
<form method="post" action="/form_submission">
	<label for="username">Username:</label>
	<input type="text" name="username" id="username">
	<label for="password">Password:</label>
	<input type="password" name="password id="password">
	<input type="submit">
</form>
```

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/form-basics' title='Form Basics'>Form Basics</a> on Learn.co and start learning to code for free.</p>
