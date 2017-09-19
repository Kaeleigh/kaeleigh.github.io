---
layout: post
title: BlocJams
feature-img: "img/Landing_Page.png"
thumbnail-path: "img/Landing_Page.png"
short-description: BlocJams a musical player!
---
## Summary
Bloc Jams is a replica of Spotify the online music player. The site has compelling features such as mobile compatibility, expansive music collection and an interactive play bar.

## Explanation
Bloc Jams was a project assigned to me as part of my web development course. Utilizing HTML, CSS, JavaScript and jQuery, I was able to build the web application that consists of three pages: landing, album, and collection. The landing page serves as the home page, the collection page showcases the variety of albums available and the album page allows users to play music from the current album selected.

## Problem
One issue I had to resolve while building Bloc Jams was converting the duration of each song from seconds to minutes and showcasing the elapse time as the song played.  

## Solution
First, I created a function named filterTimeCode that would convert the time from seconds to minutes.

        var filterTimeCode = function(timeInSeconds) {      
	         var timing = parseFloat(timeInSeconds);
	         var minute = Math.floor(timing / 60);
	         var second = Math.floor(timing % 60);
	           if (second < 10) {
		             second = '0' + second;
	          }
	         return minute + ':' + second;
	   };

The **parseFloat()** method converted the argument *timeInSeconds* into number form. The **Math.floor** method was used to round down the numbers and then stored within variables that are returned in a x:xx format. To demonstrate elapsed time I wrapped the arguments - passed within functions that handled the song’s current and total time - in the *filterTimeCode* function.

## Results
{:.center}
![]({{ site.baseurl }}/img/Album Page.png)

In the picture above, as the seekbar’s thumb moved according to the song’s playback, the elapsed time was showcased, thus success!

## Conclusion
Overall, Bloc Jams is a basic web application with some interactive features. Since this was my first web application, it was a bit challenging learning and remembering all of the fundamental concepts especially those involving JavaScript. Implementing the Buzz library in order to play actual music on the web site was intriguing and easier to navigate than jQuery library. On the landing page, I would have made the background image a slideshow of the selling points.
