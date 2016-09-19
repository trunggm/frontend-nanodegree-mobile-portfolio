## Installation
1. Go to [repo](https://github.com/trunggm/frontend-nanodegree-mobile-portfolio)
2. Clone repo or download zip.
3. Unzip(if download zip file), go to folder.
4. Run!

## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

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

## Get Solution
#### Part 1: Optimize PageSpeed Insights score for index.html
1. Minify CSS, JS file to decrease amount downlas.
2. Change Js loading block to async, expect _print.css_ with _media="print"_.
3. Resize image, change format type and compression.

#### Part 2: Optimize Frames per Second in pizza.html
Originally I just removed some of the code to make it resize faster. My next idea was to create 3 classes and apply the new classes + remove old classes to resize pizza which bought it down to about 4-8ms to resize pizza.

Finally I realised I don't have to have JS cycle through the DOM changing classes. Instead of can just create and modify the class of the container and use CSS specification to change the sizes which is much faster.

#### References
### Animation
* http://jankfree.org/
* http://www.html5rocks.com/en/tutorials/speed/animations/
* http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/

### Painting
* http://www.html5rocks.com/en/tutorials/speed/unnecessary-paints/
* http://www.html5rocks.com/en/tutorials/speed/rendering/
* http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/
* https://piazza.com/class/i0sf6tsmg0r7do?cid=1200
* http://davidwalsh.name/translate3d

### Scrolling:
* http://www.html5rocks.com/en/tutorials/speed/scrolling/

### Testing performance
* http://aerotwist.com/blog/dont-guess-it-test-it/
* http://addyosmani.com/blog/performance-optimisation-with-timeline-profiles/
* https://developer.chrome.com/devtools/docs/rendering-settings
* https://developer.chrome.com/devtools/docs/timeline

### Created JSPref's:
* http://jsperf.com/for-loop-optimisation
* http://jsperf.com/fastest-array-loops-in-javascript/329


## Now is time to run
Download and run, Now!
