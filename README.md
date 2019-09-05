# FRUI framework

The Flat & Round User Interface(FRUI)(pronounced froo-ey) is a lightweight CSS framework. Inspired by [Material UI](https://material.io) but less _materialistic_, this is my venture into building basic UI frameworks with a minimalistic and professional look.

Designed to be a lightweight, minimalistic, and developer-friendly framework, the focus shall be mainly on the following:
+ Using a separate namespace(prefix frui-* for all CSS classes) to stay flexible.
+ Reducing external dependencies.
+ Small file sizes.
+ Cross platform.
+ Easy to hack and customise.

FRUI is simple and minimalistic, and is quick to learn for somebody who already has previous experience in a framework like [Bootstrap](https://getbootstrap.com/) or [MUI](https://www.muicss.com/). This README will introduce you to the basics of the FRUI framework. A request to all the readers, I urge you to please go through the source code as well, and remember, this code is currently under development -- an ongoing effort, with many new features yet to come.

>Check [LICENSE.md](//github.com/yashdiniz/FRUI/blob/master/LICENSE.md).

## Boilerplate code
FRUI already includes [normalize.css](https://necolas.github.io/normalize.css/) which means you may keep this as the base CSS file.

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Boilerplate Code</title>
    <!-- load FRUI(assuming FRUI is stored in css/frui.css) -->
    <link href="css/frui.css" rel="stylesheet" type="text/css" />
    <!-- load custom font -->
    <link href="//fonts.googleapis.com/css?family=Roboto:300,400,500,700" rel="stylesheet" type="text/css" />
    <!-- load icon font -->
    <link href="//cdnjs.cloudflare.com/ajax/libs/font-awesome/4.2.0/css/font-awesome.min.css" rel="stylesheet" type="text/css" />
    <!-- add a custom css -->
  </head>
  <body>
    <!-- content goes here -->
    <i class="fa fa-github"></i>Hello GitHub!
  </body>
</html>
```

## Containers
FRUI containers are the simplest way to add the basic FRUI look into your webpage. FRUI containers also have [CSS grid support](https://css-tricks.com/snippets/css/complete-guide-grid/), which allows an easy layout of elements into rows and columns(no need of tables in main layout!)

The following is a basic snippet of code:
```html
<div class="frui-container">
	<h1>A simple container</h1>
	<p>Simple paragraph</p>
</div>
```

And for better grid support you can use:
```html
<!-- This CSS Grid container will be 2x2(2 rows, 2 columns) -->
<div class="frui-grid-container" style="grid-template-columns: auto auto; grid-template-rows: auto auto;">
	<!-- The first element will span the whole row(both columns of that row) -->
	<img src="picture1.png" style="grid-column-start: span 2" />
	<img src="picture2.png" />
	<img src="picture3.png" />
	<img src="picture4.png" />
	<img src="picture5.png" />
</div>
```

I would recommend beginners to check the [Complete guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) to learn more about this powerful layout, and make complete use of it.

## Dividers
FRUI dividers `.frui-divider` are a better alternative to the `<hr>` tag for horizontal dividers in HTML documents. FRUI also supports vertical dividers `.frui-divider-right`, and can be easily included into your page as shown below:
```html
<h2>Illustrating frui-dividers</h2>
<div class="frui-divider"></div>	<!-- Similar to an <hr> tag -->
<p>The thin line dividing the heading from this paragraph is called a divider!</p>
```

For right dividers:
```html
<span class="frui-text-body frui-divider-right">Illustrating right dividers</span>
<span class="frui-text-body">These elements have a divider between them!</span>
```

Divider color/width customisation:
```html
<h2>Illustrating customisability of frui-dividers</h2>
<div class="frui-divider" style="border-color: red; border-width: 3px;"></div>
<p>The thick red divider above this paragraph is very easy to customise! Here we customised the color(border-color) and width(border-width) of the divider.</p>
```

## Panels and Sections
FRUI Sections are the simplest way to make sections within your page.
```html
<div class="frui-section">
<!-- This is used to add padding to the top and bottom of this element. It helps provide a spacious look to the whole page -->
<!-- Content like panels go here -->
</div>
```

FRUI Panels are used to make the content stand out! It helps distinguish important content by putting an outline around the elements within it.

Ultimately, it is up to the developer to use Sections, Panels(or both) in a perfect combination to achieve the formatting of choice.
For example,

```html
<div class="frui-section" id="illustration">	<!-- Can use an anchor to #illustration -->
<div class="frui-panel">
	<center>
	<span style="border-color: blue;" class="frui-divider frui-text-headline">Easy and Intuitive!</span>
	<p style="width: 75%;">
		FRUI is not only easy and intuitive for the end user, but for the developer too! This little segment of code creates a nice looking, minimalistic and professional panel within a section.<br>
		This section is also tagged(using the HTML <code>id</code> attribute) and can thus be anchored as follows:<br>
		<a href="#illustration">Illustration of Panels and Sections</a>
	</p>
	</center>
</div>
</div>
```

## Tables
Tables in FRUI are implemented using the class `.frui-table`, and are coded much the same way as a normal table.
Also, if you wish to use some other table style, you can easily implement tables via the [`.frui-grid-container`](#containers)

```html
<table class="frui-table">
<thead>
<tr>	<!-- heading row -->
	<th>Table head</th>
	<th>Table head</th>
</tr>
</thead>
<tbody>
<tr>	<!-- Row 1 -->
	<td colspan='2'>A merged row spanning 2 columns</td>
</tr>
<tr>	<!-- Row 2 -->
	<td>A little more data</td>
	<td>Help illustrate tables</td>
</tr>
</tbody>
</table>
```

## Typography
FRUI also supports a minimal set of text styles that can be implemented in a webpage.
```html
<div class="frui-text-largest">Largest Text</div>
<div class="frui-text-large">Large Text</div>
<div class="frui-text-headline">Headline</div>		<!-- Similar to h1 -->
<div class="frui-text-title">Title</div>			<!-- Similar to h2 -->
<div class="frui-text-subhead">Subhead</div>		<!-- Similar to h3 -->
<div class="frui-text-body">Body</div>
<div class="frui-text-caption">Caption</div>
<div class="frui-text-menu">Menu</div>
<div class="frui-text-button">Button</div>			<!-- For button text -->
```

## Buttons
Attaching the `.frui-btn` class to any `<a>`,`<input type="button">`,`<input type="submit">` or `<button>` element.
All `.frui-btn` elements should preferably be accompanied with a CSS helper class like `.frui-btn--large`, `.frui-btn--primary` or `.frui-btn--danger`
```html
<button class="frui-btn">Default</button>	<!-- the default, flat button -->

<button class="frui-btn frui-btn--flat">Default Flat</button>	<!-- same as above, but more effective -->
<button class="frui-btn frui-btn--large">Default Large</button>	<!-- the default, flat button, but much larger -->

<button class="frui-btn frui-btn--primary">Default Primary</button>	<!-- the primary, blue button -->
<button class="frui-btn frui-btn--danger">Default Danger</button>	<!-- the danger, red button -->

<button class="frui-btn frui-btn--primary frui-btn-large">Default Large Primary</button>	<!-- a primary, large button -->

<button class="frui-btn frui-btn--primary" disabled="">Disabled</button>	<!-- This button will be disabled -->

<button class="frui-btn frui-btn--fab">+</button>	<!-- This is a Floating Action Button, designed to be a round button -->
```