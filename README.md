Easy Nav
========

A dead simple responsive navigation bar.

## What's in Easy Nav?

An index page with all the markup and jQuery needed and an  SCSS page with all the styles to get you started. That's it! 

## How do I use Easy Nav

I mentioned Easy Nav is dead simple right? Follow the next few steps and you will be on your way to stunning responsive website!

#### Step 1

Link font awesome to your style sheet

`<link href="//netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css" rel="stylesheet" type='text/css'>`

Then insert the following HTML for your navigation. Remember to edit it as you need.

		<div class="mobile"><a href="#" class="icon-reorder"></a></div>
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

The first script adds the drop down navigation.

	// change nav to drop down
	$('.mobile').on('click', function() {
		$(this).next().slideToggle(250);
		$('.menu li').on('click', function() {
			$(this).closest('.menu').slideUp(250);
		});
		return false;
	});


This second script removes a bug on desktops when resizing the browser window.

	// resize listener to show desktop nav
	$(window).resize(function() {
		var win = $(window).width();
		var menu = $('.menu')
		if (win > 700 && menu.is(':hidden')) {
			menu.removeAttr('style');
		} // back to desktop nav at 700px
	}); 

#### Step 4

Style the CSS/SCSS as you see fit! 


### Anything Else?

Nope! I message me with any potential bugs.



