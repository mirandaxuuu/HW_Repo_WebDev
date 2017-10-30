http://sites.bxmc.poly.edu/~tonglinxu/HW/Midterm/

1. Explanation

/************************
STRUCTURE
************************/

	<body>
		
		<main>

		<header>

			<h1><a href="index.html">Tonglin Xu</a></h1>

			<nav>
			</nav>

			<hr>
			
		</header>

		<article>
		</article>

		<footer>
		</footer>

		<br class="clear">

		</main>

	</body>

This part of code presents the overall layout of my website. I did not want the width of main to take over the entire page because it is too wide, but I also did not want the two sides of the page to be simply white. So I came up with an idea that I could cover the entire screen with a patterned background, and put my content in main. Therefore, the edges have their background, and the entire screen looks polished.


/**********************
PORTFOLIO NAV
**********************/

HTML:

	<div class="container">

	    <div class="view">
	    	<img src="img/studio.jpg" alt="image for music category" title="music" width="100%">
	    		<a href="music.html"><h2>Music</h2></a> 
	    </div>

	    <div class="view">
	    	<img src="img/camera.jpg" alt="image for photography category" title="photography" width="100%">
	    		<a href="photography.html"><h2>Photography</h2></a> 
	    </div>

	    <div class="view">
	    	<img src="img/xbox.jpg" alt="image for games category" title="games" width="100%">
	    		<a href="games.html"><h2>Games</h2></a> 
	    </div>

	</div>


CSS:

	.view {
		cursor: default;
		text-align: center;
		position: relative;
		margin-bottom: 30px;
	}

	.view a {
		width: 100%;
		height: 100%;
		position: absolute;
		top: 0;
		left: 0;
		bottom: 0;
		right:0;
		background-color: rgba(0,0,0,0.7);
		/* this makes the contaner a flex box*/
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-decoration: none;
	}

	.view img {
		display: block;
		position: relative;
	}

	.view h2 {
		color: white;
		font-size: 36px;
	}


	.view img {
		transition: all 0.2s ease-in-out;
	}

	.view a {
		transition: all 300ms linear;
		opacity: 0;
	}

	.view h2 {
		color: white;
		transition: all 600ms linear;
		opacity: 0;
	}

	.view:hover img {
		opacity: 0.5;
	}

	.view:hover a {
		opacity: 1;
	}

	.view:hover h2,
	.view:hover p,
	.view:hover a {
		opacity: 1;
	}


I had a really hard time dealing with my portfolio navigation. I wanted it to be dymanic: it displays images by defult, and when I hover over the images, the image darkens and the title is displayed over the image. 

At first I was struggling with putting my title at the center of the image. If I do "text-align: center", that would only center it horizontally but not vertically. If I do abosolute and relative positions like how we did the gallery page in class, and set the value of the top margin, when I change the size of my browser, the title would no longer be at the middle. In the end Professor told me that I could use a technique called "flex box". I can set the content at the center by declaring "justify-content: center" and "align-items: center". 

I was also struggling with the size of the clickable area. At first, I could only click on the text to be nevigated accordingly. Later I figured out that I could stretch the anchor tags to be the same sizes as the images, so that I could click on the entire image to be directed to other pages. I did this by using absolute and relative position. When the images are "position relative", the anchor tags are "position absolute" and both top and left are set as 0.


/***************************
SIDEBAR
***************************/

	<div class="sidebar">
		<nav>
			<ul>
				<li><a href="#cityimg">City</a></li>
				<li><a href="#lsimg">Landscape</a></li>
				<li><a href="#ptimg">Portrait</a></li>
				<li><a href="#mtimg">Montage</a></li>
			</ul>
		</nav>
	</div>

	<div class="container">
		<div class="polaroid" id="cityimg">
			<img src="photography/city1.jpg">
		</div>
		<div class="polaroid">
			<img src="photography/city2.jpg">
		</div>
		......
	</div>


In my photography page, I created a sidebar for navigation. I assigned the IDs for the images accordingly, and in the navigation bar I put links to the IDs. In my CSS file I also set this sidebar to be "position fixed", so it sticks at the top left corner of the page and does not go down when I scroll the page.

At first, this page worked extremely slow. I figured out that it is because my image sizes are large. I used photoshop to reduce the size of the image and solved the problem.



2. Reflection

When I was creating my music page, I first tried to use the 996 grid. However, as I finished styling the page with 996 grid, I felt like this page looked too much like a "grid". Everything was perfectly aligned in grids so it looked rigid. In the end I discarded this page and rewrote it without uing 996 grid, and it looked better for me. Maybe I encountered this issue because I still do not have enough skill to use the grid in a flexible way. This is also something that I want to learn more if I had more time.

I taught myself about how to embed YouTube videos in my website. I learned about the functions of some of the parameters, such as how to change the color of the player control, how to allow fullscreen, and how to hide the YouTube logo. I attempted to change the color of the big play button from red to grey, but I failed. In the end I learned that I could not change this setting with parameter.

I also learned about embedding font awesome icons in my webpage. I used them in my contact page. At first the idea of using the icons did not come to my mind. I simply displayed my contact informations in a list, but when I showed it to my friends, they said that they did not think that they could actually click on the informations to see more. (Something I found useful is to let my friends test my website to see if the interaction is intuitive.) Then I tried to put the underline below the words, but did not look elegant. In the end, I used the icons because they look good and they are very discriptive. 

I realized most of my ideas that I had at the beginning. In this process, not only did I teach myself some new techniques that we did not cover in class, but also did I review what we learned and actually put them into practice. One thing that was in my plan that I did not have time to do is to have a background music for my website. If I had more time and tools, I would want to improve this.