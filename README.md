# Meteor-Tutorial
A short Todo app following Meteor's online tutorial

## Lesson 1: Creating an App

  * Install Meteor, then simply type `meteor create <app_name>`
  * Relevant files are initialized!

## Lesson 2: Templates ([Branch: lesson_2](https://github.com/melodicodyssey/Meteor-Tutorial/tree/lesson_2))

  * In addition to parsing standard `head` and `body` sections of the HTML files, Meteor looks for, and compiles, its own __templates__ included in special `template` tags(in the top level of the HTML.

  * Templates are Meteor's way of binding data and adding logic to the view.  From the Meteor docs:

    > Templates are defined in `.html` files that can be located anywhere in your Meteor project folder except the server, public, and private directories.
    >
	> Each .html file can contain any number of the following top-level elements: `<head>`, `<body>`, or `<template>`. Code in the `<head>` and `<body>` tags is appended to that section of the HTML page, and code inside `<template>` tags can be included using `{{> templateName}}` ... Templates can be included more than once — one of the main purposes of templates is to avoid writing the same HTML multiple times by hand.

	* This means that you may define a template in any `.html` file, and access it anywhere else in your project.  At first glance, as a newcomer to Meteor, this leads me to believe that I can dedicate a single `.html` file to contain some/most/all of my templates for use in my other files, for organizational purposes.

	  * Exaple: as seen in [this commit on branch `lesson_2`](https://github.com/melodicodyssey/Meteor-Tutorial/commit/f7218d836c716d9eab096e9adc678c6c1dc1257c), I created introduced a new template, named `foo`, that simply outputs `<span>Hello World</span>`.  this template was succesfully called when I placed `{{> foo}}` with the rest of the content within the `body` tag.

    * The `{{ ... }}` syntax is part of a language Meteor uses, called [Spacebar](http://meteorcapture.com/spacebars/).

  * But templates don't often exist in the HTML alone; a major advantage Meteor brings is to create `helper`s that bind to these templates in your JavaScript files.