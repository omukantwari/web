## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html
To accomplish this part of project, I performed the following: Minified print and style CSS files, Minified perfmatters JS file, Inlined style.css, added media = “print” to print.css link, added “async” to google analytics.com script, resized and compressed pizzeria.jpg, and compressed profilePic.jpeg
To verify PageSpeed score, I hosted page on github. The page address is (http://ed-ramos.github.io/frontend-nanodegree-mobile-portfolio). . To see results, add this address to Google’s PageSpeed Insights page located at (https://developers.google.com/speed/pagespeed/insights/)

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

To accomplish this part of project, I first used Chrome’s Dev Tools to record measurements as I scrolled through page and used the pizza size slider.
On the ChangePizzaSizes function, replaced querySelectorAll method with the more efficient getElementsbyClassName method.  calculate the dx and newwidth variables outside of the for loop as its values does not change as i changes.  Also, create variables outside of for loop so that document is referred to once and not multiple times inside loop.
On the UpdatePositions function,  calculate the five unique phase values outside of main for loop and place them in an array. Replaced querySelectorAll method with the more efficient getElementsbyClassName method. Create variable outside of loop so that document is accessed once and not multiple times.
Finally, changed code so that instead of 200 sliding pizza being generated when page loads, only 40 are generated. This should cover the number of pizzas that are visible on screen.