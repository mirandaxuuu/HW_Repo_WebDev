WebDev Final Project

http://sites.bxmc.poly.edu/~tonglinxu/HW/Week_12_Final/

Changes I made:

1. Cover Page & Slideshow
In my final project proposal, I said that I want to make a cover page and I also want to try slideshow. I ended up putting them together so it becomes a cover page with a slideshow. I used Bootstrap carousel to build this page.

2. Opening quotes
My new opening quotes can switch between two different quotes every 4 seconds. I used JavaScript and JQuery to toggle the quotes.

<code>
	var quoteToggle = true;
	var myQuote; 
	document.addEventListener('DOMContentLoaded', function () {
		myQuote= document.getElementById('myquote');
		setInterval(myFunction, 4000);		
	});

	function myFunction () {
		//console.log(myQuote);
		quoteToggle = !quoteToggle;
		console.log(quoteToggle);
		if (quoteToggle) {
			myQuote.innerHTML= '"To send light into the darkness of men\'s hearts - such is the duty of the artist." - Robert Schumann';
		} else {
			myQuote.innerHTML= '"Works of art make rules; rules do not make works of art." - Claude Debussy';
		}
	}
</code>


3. Background Music
I added a background music for the homepage using the audio tag in HTML.

<code>

	<audio autoplay="" controls="" loop="" preload="">
		<source src="audio/Departure.wav" type="audio/wav"></source>
	</audio>

</code>

4. Top Button
I added a button at the lower right corner on all pages that links to the top of the page. I used the TweenLite in GSAP to get the smooth scrolling effect.

<code>
	$(document).ready(function() {
	    $('#gotop').click(function(){
	        TweenLite.to(window, 0.5, {scrollTo:0});
	    });
	});
</code>


5. Contact
I made an animated timeline using GSAP TimeLineLite. The list items fade in one by one. I also added my resume to the contact page, according to the feedback I got from midterm.

<code>
	$(document).ready(function(){
		var
		$email = $('li').eq(3),
		$tumblr = $('li').eq(4),
		$youtube = $('li').eq(5),
		$weibo = $('li').eq(6),
		$facebook = $('li').eq(7),
		$resume = $('li').eq(8),
		$bg = $('#page-wrap');

		var tl = new TimelineLite();

		tl.from($bg, 0.8, {opacity:0})
		.from($email, 0.5, {opacity:0})
		.from($tumblr, 0.5, {opacity:0})
		.from($youtube, 0.5, {opacity:0})
		.from($weibo, 0.5, {opacity:0})
		.from($facebook, 0.5, {opacity:0})
		.from($resume, 0.5, {opacity:0})
	});
</code>

6. Game Download
I used to provide a Google Drive link to my first game, but then the users would be linked to a ugly Google Drive page. I changed the href of my anchor tag so that the users are now directly linked to the download page when they click on my game title.


7. Interactive footer

When users click on the footer under contact page, the footer would shake for 3 times. This interactivity is just for fun.

<code>
	var $myFooter = $('.interactive');
	$myFooter.click(function(){
		$myFooter.effect("shake", {times:3}, 1000);
	});
</code>


Future improvement:

1. I got a feedback from midterm presentation that I should have a dropdown menu in my navbar. I tried to do this for my final project, but each time when I added the dropdown menu, it broke my entire page layout. In the end, I gave up this idea because I did not have enough time to figure it out. If I had more time, I would like to fix this problem because I know that we have learned many ways to do it.

2. I used Bootstrap for my cover page, but I don't really like the way it looks because it looks like every other website. I want to find a way to personalize my cover page.


Problems I encounted and things I learned: 

1. When I tried to use GSAP TweenLite, I had a hard time making it scroll to top, because in the class example, we had it scroll to a specific element. I went through the TweenLite guide and in the end, I realized that it was much simpler than I thought.

2. I wanted to overlay my "enter site" button on top of my carousel, so I did some research on carousel overlay.

3. I learned about the shake effect in jQuery to add the shake effect to my footer.