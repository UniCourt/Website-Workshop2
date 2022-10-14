# Create CSS file and link it to the Web page
## # create dir
Create a directory name `css` under `simple-blog/src`
create a file `style.css` under `simple-blog/src/css`
### Link the css file to the web page
Add this code inside the head tags of both the web pages
```html
<head>
...
<link rel="stylesheet" href="css/style.css" />
...
</head>
```
# Reset CSS
- A reset stylesheet (or CSS reset) is a collection of CSS rules used to clear the browser's default formatting of HTML elements, removing potential inconsistencies between different browsers. It also prevents developers from unknowingly relying on the browser default styling and force them to be explicit about the styling they want to apply on the page.

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&display=swap');
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
img {
    height: auto;
    max-width: 100%;
}
a {
    color: #1565c1;
    cursor: pointer;
    text-decoration: none;
}
```

# Body tag
The `<body>` tag defines the document's body.
The `<body>` element contains all the contents of an HTML document, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
**Note:** There can only be one `<body>` element in an HTML document.
### Example:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>HTML & CSS Learning Workshop Blog</title>
        <link rel="stylesheet" href="css/style.css" />
    </head>
    <body>
		
    </body>
</html>
```
```css
body{
    font-family: Roboto,"Segoe UI",Oxygen,Ubuntu,Cantarell,"Fira Sans","Droid Sans","Helvetica Neue",Helvetica,Arial,BlinkMacSystemFont,-apple-system,sans-serif;
    color: #4a4a4a;
    font-size: 1em;
    font-weight: 400;
    line-height: 1.5;
}
```

### header tag
The `<header>` element represents a container for introductory content or a set of navigational links.
```html
<header>

</header>
```

### nav tag
The `<nav>` tag defines a set of navigation links.
Notice that NOT all links of a document should be inside a <nav> element. The <nav> element is intended only for major blocks of navigation links.
```html
<nav>

</nav>
```
### Example: 
Insert this code inside the body tag
```html
<header>
	<nav id="main-nav" class="navbar">
		<div class="container">
			<div class="navbar-brand">
				<a class="navbar-item" href="#">
					<img src="./images/logo.png" alt="UniCourt">
				</a>
				<div class="navbar-burger burger" id="nav-toggle">
					<span></span>
					<span></span>
					<span></span>
				</div>
			</div>

			<div id="navbar-example" class="navbar-menu">
				<div class="navbar-end">
					<a class="navbar-item" href="#">Home</a>
					<a class="navbar-item" href="#">Features</a>
					<a class="navbar-item" href="#">Industries</a>
					<a class="navbar-item" href="#">Pricing</a>
					<a class="navbar-item is-active" href="index.html">Blog</a>
					<a class="navbar-item" href="#">Sign Up</a>
				</div>
			</div>
		</div>
	</nav>
</header>
```
```css
#main-nav{
    border-bottom: solid rgba(0,0,0,.2) 1px;
}
#main-nav>.container{
    align-items: stretch;
    display: flex;
    min-height: 3.25rem;
    width: 100%;
}
.navbar-menu .navbar-end {
    align-items: center;
}
.navbar-item{
    color: #4a4a4a;
    display: block;
    line-height: 1.5;
    padding: 0.5rem 0.75rem;
    position: relative;
}
.navbar-item.is-active{
    color: #205c9a;
}

@media screen and (min-width: 1088px){
    .navbar, .navbar-end, .navbar-menu{
        flex-grow: 1;
        flex-shrink: 0;
    }
    .navbar, .navbar-end, .navbar-menu {
        align-items: stretch;
        display: flex;
    }
    .navbar-end {
        justify-content: flex-end;
        margin-left: auto;
    }

    .navbar-item{
        align-items: center;
        display: flex;
    }
}


@media screen and (max-width: 768px){
    #main-nav>.container{
        padding: 0;
    }
    .navbar-menu{
        position: absolute;
        background-color: #fff;
        border-bottom: solid rgba(0,0,0,.2) 1px;
        left: 0;
        right: 0;
        top: 77px;
        box-sizing: border-box;
        display:none;
    }
    .navbar-menu.is-active{
        display: block;
    }
    .navbar-brand{
        display: flex;
        flex-grow: 1;
        align-items: center;
    }
    .navbar-brand .navbar-item{
        padding: 0;
    }
    .navbar-burger {
        width: 3rem;
        display: block;
        cursor: pointer;
        margin-left: auto;
    }
    .navbar-burger span {
        height: 2px;
        background-color: #1565c1;
        display: block;
        width: 16px;
        margin-bottom: 4px;
    }
}
```


# Container
```html
<div class="container">
</div>
```
```css
.container {
    margin: 0 auto;
    padding-left: 0.75rem;
    padding-right: 0.75rem;
    box-sizing: border-box;
}
@media screen and (min-width: 1472px){
    .container {
        max-width: 1344px;
    }
}
```

# Wrapper
```html
<div class="wrapper">

</div>
```
```css
@media screen and (min-width: 769px){
    .wrapper {
        display: flex;
    }
}
```

# Section tag
The `<section>` tag defines a section in a document.
```html
<section id="primary">

</section>
```
```css
@media screen and (min-width: 769px){
    #primary{
        flex: none;
        width: 66.66667%;
        padding-right: 24px;
    }
}
```

# Article tag
The `<article>` tag specifies independent, self-contained content.
An article should make sense on its own and it should be possible to distribute it independently from the rest of the site.
### Example: 
```html
<article id="post-1">
	<div class="post-image">
		<a href="./single-post.html" title="Lorem ipsum dolor sit amet, co">
			<img src="./images/post-1.avif" alt="Lorem ipsum dolor sit amet, co" width="868" height="579">
		</a>
	</div>
	<div class="post-content">
		<div class="post-details">
			<h2 class="title"><a href="./single-post.html" rel="bookmark">Lorem ipsum dolor sit amet, co</a></h2>
			<p class="post-meta">
				<span class="wrap-posted-on">
					By <a href="#">UniCourt</a>
					on <time datetime="2022-10-10T05:55:53-08:00">October 10, 2022</time>
				</span>
			</p>
		</div>
		<div class="content">
			<p>
				Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium. Integer tincidunt. Cras dapibus. Vivamus elementum semper nisi. Aenean vulputate eleifend tellus. Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim. Aliquam lorem ante, dapibus in, viverra quis, feugiat a, tellus. Phasellus viverra nulla ut metus varius laoreet. Quisque rutrum. Aenean imperdiet. Etiam ultricies nisi vel augue. Curabitur ullamcorper ultricies nisi. Nam eget dui. Etiam rhoncus. Maecenas tempus, tellus eget condimentum rhoncus, sem quam semper libero, sit amet adipiscing sem neque sed ipsum...
			</p>
			<a href="./single-post.html" rel="bookmark">Read More...</a>
		</div>
	</div>
</article>
```
```css
article{
    border-bottom: solid rgba(0,0,0,.2) 1px;
    margin-top: 32px;
    padding-bottom: 32px;
}
article .title {
    font-size: 1.5rem;
    font-weight: 600;
    line-height: 2;
}
article .title a{
    color: #363636;
}
article .card-image img{
    min-width: 100%;
}
article .card-content{
    padding-top: 16px;
}
article .card-content .media{
    margin-bottom: 1.5rem;
}
article .post-meta{
    font-size: .75rem;
}
article .post-meta .wrap-posted-on{
    display: block;
    margin-bottom: 8px;
}
```

# Sidebar - aside tag
The `<aside>` tag defines some content aside from the content it is placed in.
The aside content should be indirectly related to the surrounding content.
The `<aside>` content is often placed as a sidebar in a document.
### Example
```html
<aside id="secondary" class="column">
	<div id="recent-posts">
		<div class="widget-content">
			<h3 class="heading">Recent Posts</h3>
			<ul>
				<li>
					<a href="./single-post.html">Lorem ipsum dolor sit amet, co</a>
				</li>
				<li>
					<a href="./single-post.html">Lorem ipsum dolor sit amet, consectetuer</a>
				</li>
				<li>
					<a href="./single-post.html">Lorem ipsum dolor si</a>
				</li>
				<li>
					<a href="./single-post.html">Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</a>
				</li>
				<li>
					<a href="./single-post.html">Lorem ipsum dolor sit amet, consectetuer adipiscin</a>
				</li>
			</ul>
		</div>
	</div>
</aside>
```
```css
aside{
    padding-left: 24px;
    padding-top: 32px;
    border-left: solid rgba(0,0,0,.12) 1px;
}
aside{
    border-bottom: solid rgba(0,0,0,.12) 1px;
    padding-bottom: 32px;
    margin-bottom: 32px;
}
aside .heading{
    font-size: 1.25rem;
    color: #205c9a;
    margin-bottom: 16px;
}
#recent-posts ul {
    list-style: disc;
    padding-left: 32px;
}
#recent-posts ul li{
    margin-bottom: 16px;
}
#recent-posts ul a{
    color: inherit;
}
```

# Footer
The `<footer>` tag defines a footer for a document or section.
**A `<footer>` element typically contains:**
- authorship information
- copyright information
- contact information
- sitemap
- back to top links
- related documents

### Example
```html
<footer>
	<div class="container">
		<div>
			<nav class="hide-on-signup">
				<a href="#">Footer link</a>
				<a href="#">Footer link</a>
				<a href="#">Footer link</a>
			</nav>
		</div>
		<div class="is-hidden-mobile">
			<p>
				© 2022 mysite.com
			</p>
		</div>
	</div>
</footer>
```
```css
footer{
    border-top: 1px solid rgba(0,0,0,.2);
}
footer{
    border-top: 1px solid rgba(0,0,0,.2);
    text-align: center;
    font-size: 14px;
    padding: 8px 0;
}
footer a{
    color: inherit;
    margin: 0 4px;
}
```