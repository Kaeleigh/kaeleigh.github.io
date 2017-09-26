---
layout: post
title: Lite Brite
feature-img: "img/LiteBrite.png"
thumbnail-path: "img/LiteBrite.png"
short-description: Lite Brite an interactive drawing game!

---
## Summary
  Lite Brite is a replica of the popular children's game Lite-Brite. Similar to the original game, users can create pictures by choosing various colors, selecting empty dots and clicking the blink button.
## Explanation
The Lite Brite project was apart of the JavaScript course on [CodeAcademy](https://www.codeacademy.com). My assignment was to add functionality to the game using JavaScript and jQuery. First I created a function that would categorize all game functionality. To allow users to select a particular color, I created an click handler on the color elements that held a certain class. Within the handler I, utilized a switch statement to define the colors for the boxes. Also created another click handler that would allow users to flash their pictures once they clicked on the blink button.
## Problem
When users clicked the blink button, the selected cells had to flash based on the colors chosen by the user.
## Solution
To resolve this issue I used a conditional statement within the blinking click function that would change the value of colorClass to the color that was selected by the user. Then using jQuery's `.toggleClass()` attribute I placed a new class on the blinking element as well as the colored boxes so that the opacity of the cells would flash once the blink button was clicked.

          $('.toggle-blink').on('click', function() {
             if(colorClass) {
               $('.toggle-blink').toggleClass('opacity');
               setInterval(function() {
                 $('.box.blue, .box.yellow, .box.orange').toggleClass('blink');
                }, 350);
               }
            });   


Furthermore I used the `setInterval` function to automatically toggle the opacity of selected elements every .35 seconds.

## Results

{:.center}
![]({{ site.baseurl }}/img/blink1.png)

{:.center}
![]({{ site.baseurl }}/img/blink2.png)

In the two pictures above the selected cells toggle between an opacity of 0.7 seen in the first picture, and opacity of at 1 seen in the second picture. Thus, after clicking the blink button the flashing of the selected cells was successful.
## Conclusion
This was a fun project to contribute on because it is an interactive game. Utilizing jQuery to refactor some JavaScript functions made the process a bit smoother. I liked that one could customize their version of the game by changing the color choices. What can you create? Give [LiteBrite](https://codepen.io/fandmgrl/full/eGZmYr/) a try.
