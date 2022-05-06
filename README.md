# 11056 Website 2
## _Reflection and Code for front end web design_

### Reflection

##### Thoughts on Eleventy
Upon reflection of this task I would like to primarily compare my past experience with the Glitch coding website / aplication and visual Studio code to the one I had with this assignment with the intergration of Eleventy.

Straight up, sorry but its a no for Eleventy, though I understand where it certainly has its conveniences ( if you can figure out how to use it ) compared to the method used in the previous assignment and especially on large scale use. My main reason for disliking eleventy is that every time I changed something in my html files and ref refreshed the page it would delete all of my css so I was constantly having to paste my code into another application such as pages so I didn’t lose it, or risk spamming command Z. In brief I believe many of the problems I encounter aside from the one I just mentioned and the program crashing leaving me with no choice but have to keep setting up everything in the terminal again, where my own. - did i mention it wouldnt let me delete files e.g the Java script one.

Im willing to come clean and admit I’m still not really sure on how all the files talk to one another especially the index markdown file. I felt like I was able to make the page work without needing the markdown file at all and when I tried to use it I found that I always had doubles of things or I couldn’t figure out how to make the footer stay at the bottom of the page and not duplicated resulting in one of them combining with the header. In hindsight I wish I had played around with a more detailed template as I believe that, that may have allowed me to get a better understanding of what is actually happening.

#### Website & Code

Similarly to the last assignmentI found that, for lack of better words, this work slowly grew into itself as by using my low fidelity prototypes and my initial code I quickly had a scaffolding of what the website was doing too look like, although this time I tried about 4 different layouts and decided I liked the final one with the hero image the most as I believe I did a better job with the colours and the proportions of the layout… felt like it was more realistic and easier to interact with. 

I will finish on what i belive to be my most annoying issue which is, that for one of my draft layouts I tried to code in a hero image with Image thumb nails below it and sadly with little success, I managed to get what i belived to be the html and css to work though not the javascript which i will attach below. In a very brief conclusion I found that this assignment had an added amount of comoplexity to it than the previous one and that if i could do it again i would spend more time looking into how the differnt files operate in a more sophisticated template.

```
let slideIndex = 1;
showSlides(slideIndex);

// Next/previous controls
function plusSlides(n) {
  showSlides(slideIndex += n);
}

// Thumbnail image controls
function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("demo");
  let captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
```