Easy Nav
========

A dead simple responsive navigation bar.

## What's in Easy Nav?

An index page with all the markup and jQuery needed and an  SCSS page with all the styles to get you started. That's it! 

## How do I use Easy Nav

I mentioned Easy Nav is dead simple right? Follow the next few steps and you will be on your way to stunning responsive website!

#### Step 1

Link font awesome to your style sheet. Font awesome is used to generate the navigation icon on mobile. This step is optional.

`<link href="//netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css" rel="stylesheet" type='text/css'>`

Then insert the following HTML for your navigation. Remember to edit it as you need.

		<a href="#" id="mobile-icon" class="icon-reorder"></a>
		<nav class="menu">
			<li><a href="#">Nav Item 1</a></li>
			<li><a href="#">Nav Item 2</a></li>
			<li><a href="#">Nav Item 3</a></li>
			<li><a href="#">Nav Item 4</a></li>
			<li><a href="#">Nav Item 5</a></li>
		</na>

#### Step 2

Add jQuery to your website. I like to use the following CDN

`<script type="text/javascript" src="http://code.jquery.com/jquery-latest.min.js"></script>`

#### Step 3

Add the jQuery magic!

The first script adds variables used through the code and creates a drop down toggle function.

	// variables for navigation
	var win = $(window).width();
	var menu = $('.menu');
	var menuLink = $('.menu a')

	// toggle drop down function
	function toggleDropDown() {
		$('nav').slideUp(250);
	}

The second script creates the open/close drop down effect.

	// opens and closes mobile drop down
	$('#mobile-icon').on('click', function() {
		$(this).next().slideToggle(250);
		menuLink.on('click', toggleDropDown);
		return false;
	});


This third script removes a bug on desktops when resizing the browser window.

	// resize listener to show desktop nav
	$(window).resize(function() {
		if (win > 560 && menu.is(':hidden')) {
			menu.removeAttr('style');
			menuLink.off('click', toggleDropDown);
		}
	});

#### Step 4

Style the CSS/SCSS as you see fit! 


### Anything Else?

Nope! I message me with any potential bugs. In the next update I will convert the jQuery into a plugin so it's even easier to add to your site!



