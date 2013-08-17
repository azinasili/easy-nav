Easy Nav
========

A dead simple plugin to add responsive navigation.

## What's in Easy Nav?

* An html page with an example of Easy Nav.
* The jQuery plugin, both development and production versions.
* CSS/SCSS to edit navigation styles.

## How do I use Easy Nav

I mentioned Easy Nav is dead simple right? Follow the next few steps and you will be on your way to stunning responsive website!

#### Step 1

Link font awesome to your style sheet. Font awesome is used to generate the navigation icon on mobile. This step is optional.

`<link href="//netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css" rel="stylesheet" type='text/css'>`

Then insert the following HTML for your navigation. Remember to edit it as you need.
	
	<div class="nav"> 
		<a href="#" class="mobile-icon icon-reorder"></a>
		<nav class="main-nav">
			<li><a href="#">Nav Item 1</a></li>
			<li><a href="#">Nav Item 2</a></li>
			<li><a href="#">Nav Item 3</a></li>
			<li><a href="#">Nav Item 4</a></li>
			<li><a href="#">Nav Item 5</a></li>
		</nav>
	</div>

#### Step 2

Add jQuery and the Easy Nav plugin to your website. I like to use the following CDN

`<script type="text/javascript" src="http://code.jquery.com/jquery-latest.min.js"></script>`

`<script type="text/javascript" src="your/path/to/jquery.easy-nav.min.js"></script>`

#### Step 3

Add the jQuery magic!

The first script adds variables used through the code and creates a drop down toggle function.

	<script>
		$(document).ready(function() {
			$('.nav').easyNav();
		});
	</script>

#### Step 4

Style the CSS/SCSS as you see fit! 


### Anything Else?

Nope! I message me with any potential bugs. In the next update I will convert the jQuery into a plugin so it's even easier to add to your site!



