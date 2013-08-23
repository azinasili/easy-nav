Easy Nav
========

A dead simple plugin to add responsive navigation.

## What's in Easy Nav?

* An html page with an example of Easy Nav.
* The jQuery plugin, both development and production versions.
* CSS/SCSS to edit navigation styles.

## How do I use Easy Nav

I mentioned Easy Nav is dead simple right? Follow the next few steps and you will be on your way to stunning responsive website! [View Easy Nav in action here](http://azinasili.com/easy-nav/).

#### Step 1

Link font awesome to your HTML, right after your linked CSS should be fine. Font awesome is used to generate the navigation icon on mobile. This step is optional.

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

Add jQuery and the Easy Nav plugin to your website. Best to place these right before the closing body tag. I like to use the following CDN.

`<script type="text/javascript" src="http://code.jquery.com/jquery-latest.min.js"></script>`

`<script type="text/javascript" src="your/path/to/jquery.easy-nav.min.js"></script>`

#### Step 3

Add the jQuery magic! Place the jQuery call right after the Easy Nav plugin

	<script>
		$(document).ready(function() {
			$('.nav').easyNav();
		});
	</script>

#### Step 4

Add the CSS for your navigation! Remember to edit the CSS to fit your needs.

	.icon-reorder {
		color: #ebebeb;
		cursor: pointer;
		font-size: 0;
		float: right;
		position: relative;
		top: 2.25rem;
	}

	.main-nav {
		float: right;
	}

	.main-nav li {
		display: inline;
		margin-right: 25px;
	}

	.main-nav li:last-child {
		margin-right: 0px;
	}

	.main-nav li a {
		color: #ebebeb;
		font-size: 1rem;
		font-weight: 400;
		text-decoration: none;
		-webkit-transition: color 0.3s;
		-moz-transition: color 0.3s;
		transition: color 0.3s;
	}

	.main-nav li a:hover {
		color: #9FC7E3;
	}

    @media screen and (max-width: 44rem) {
        .icon-reorder {
            font-size: 1.5rem;
        }

        .main-nav {
            background: #333333;
            display: none;
            position: absolute;
            top: 6rem;
            left: 0rem;
            width: 100%;
        }

        .main-nav li {
            display: block;
            border-bottom: 1px solid black;
            line-height: 5rem;
            margin-left: 25px;
        }

        .main-nav li a {
            color: #ebebeb;
            display: block;
            height: 100%;
            width: 100%;
        }
    }


### Anything Else?

Nope! Message me with any potential bugs.



