# Project: mi-bo &nbsp;&nbsp;&nbsp; :evergreen_tree:

<br>

### Greetings, MINDBODY member! &nbsp; &nbsp; &nbsp; 

<br>

### Objectives
  - use <a href="https://fonts.google.com/specimen/Lato" target="_blank">__Google Lato__</a> font
  - configure sign up button
    - hover state
    - trigger form validation upon click
  - insert current year before "Company" in footer
  - transform a given screenshot into code: <a href="https://github.com/vandoan/mi-bo/blob/master/misc/webinar_screenshot.png" target="_blank">_/misc/webinar_screenshot.png_</a>
  - additional details: 
    
    - <a href="https://github.com/vandoan/mi-bo/blob/master/misc/original_README.md" target="_blank">_/misc/original_README.md_</a>
    - the assignment's  <a href="https://github.com/MINDBODY-FEE/homework-marketing" target="_blank">__Git repository__</a>

<br>

### Tools

  - Macbook 12 in.
  - Sublime text editor
  - CSS and HTML validators
  - surf ipsum from an <a href="http://dijiworkshop.com/surf_ipsum/" target="_blank">__old project__</a>
  - Chrome browser and inspector tool
  - Firefox browser and <a href="https://hacks.mozilla.org/2017/06/new-css-grid-layout-panel-in-firefox-nightly/" target="_blank">__grid layout tool__</a> (_magical!_)
  - <a href="https://necolas.github.io/normalize.css/" target="_blank">__Normalize CSS__</a> to reset default configurations</a>
  - Pixelmator for cutting images, counting pixels, and obtaining colors

<br>

### Up and running
You can temporarily view 
<br> the page on my <a href="http://vandoan.github.io/" target="_blank">__Github static page__</a>.
<br>
<br>

### Upon comparsion 
The page should look nearly identical 
<br> to the webinar screenshot. Some things to keep in mind.

  - Firefox 56.0 checks out
  - Safari requires version 10.3^
  - Chrome version 60.0.3^ for optimal resolution
  - minimum window width: 1278 pixels (larger than this Macbook screen, womp-womp)
  - for other browsers and versions, the grid CSS property is necessary, so check with <a href= "http://caniuse.com/#feat=css-grid" target="_blank">caniuse.com grid compatibility chart</a>

<br>

### Measurements &nbsp;&nbsp;&nbsp; :triangular_ruler:

- check out the <a href="https://github.com/vandoan/mi-bo/blob/master/misc/measurements.png" target="_blank" />__measurements file__</a> 
  - <a href="https://github.com/vandoan/mi-bo/blob/master/misc/measurements.png" target="_blank" />_/misc/measurements.png_</a>
- this holds all of the initial measurements:
 	<br>heights, widths, font colors, margin spacings, 
  <br>background colors, border colors, font heights, line heights

-  _* Note, some of the initial measurements were not accurate, 
<br> so many have been updated to their true values,
<br> and this doc does not reflect those updates._

<br> 

### Final Product &nbsp;&nbsp;&nbsp; :package:

<br>

###### Webinar original screenshot
<br>![Webinar screenshot](https://raw.githubusercontent.com/vandoan/mi-bo/master/misc/webinar_screenshot.png)

<br> 
<br>

###### Reproduction screenshot &nbsp;&nbsp;&nbsp; :star:
<br>![Webinar duplicate screenshot](https://raw.githubusercontent.com/vandoan/mi-bo/master/misc/webinar_duplicate.png)

<br>
<br>

###### Webinar comparison screenshot, original on left and reproduction on right
<br>![Webinar comparison screenshot](https://raw.githubusercontent.com/vandoan/mi-bo/master/misc/webinar_comparison.png)

<br>
<br>
<br>
<br>
<br>

## Personal Preferences / Idiosyncrasies / Code Walk-Through

<br>

### CSS ordering
 CSS properties are stacked by __length, shortest to longest__, 
 <br> as long as there's no ill effects from the ordering. Plus, it's pleasant on one's eyes.
        
    nav {
  	     height: 40px;
  	     font-size: 1em;
  	     text-align: left;
   	     background-color: #232329;
    }

<br>

### Attribute naming convention 
__Parent__ component divs get __longer names__ and can come with 
<br>an __abbreviated name__ as well. 
__Children__ get __abbreviated names__.
<br>

__HTML__:
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; \<section class="__course-desc cd__">
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; \<h2>Course description</h2>... \</div> ...
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<p>...\</p>...
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; \</section>

__CSS__:
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; section.__course-desc__ { grid-column: 1/9; }
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.__cd__ h2 { color: #232329; ... }

<br>

### CSS and KISS

  - <a href="https://en.wikipedia.org/wiki/KISS_principle" target="_blank">__keepin' it simple__</a> principle
  - with CSS, 3 or fewer levels deep, _no mas, por favor._ 
  - no id attributes were used, as they weren't necessary
  - with JavaScript, id attribute use is more suitable
  - note, a <a href="https://stackoverflow.com/questions/31026901/processing-speed-difference-between-css-class-and-id" target="_blank">__tiny speed difference__</a> between id's and classes, but not large enough to warrant id use

<br>

### Clear structure &nbsp; &nbsp; &nbsp; :musical_score:
Break HTML into core components and sections, 
<br> lessons from React.js. Also, HTML components are similar to divs.
<br>

    Structure
                general:          outer shell   |  inner shell  |  content
                div:              margin        |  padding      |  content
                HTML structure:   component(s)  |  section(s)   |  content
                HTML:             <header>      |  <section>    |  <div class="eyebrow">
    
    HTML:       <header>
                    <section>
                        <div class="eyebrow">WEBINAR</div>
                        ...
                    </section>
                </header>

<br>

### Purpose and divs
Every div has a purpose.

  - clear and concise
  - clean and lean HTML
  - review code and remove purposeless divs

<br>

### Readability and HTML5 elements &nbsp; &nbsp; &nbsp; :book:
The use of HTML5 new elements makes 
<br> code clearer and easier to read and navigate. 

  - <a href="https://www.w3schools.com/html/html5_semantic_elements.asp" target="_blank">__HTML5 Elements__</a>
  -  \<main>\, \<footer>\, \<nav>\, and many more

<br>

### Grid CSS property 
Trade offs here, a hard call on whether to use it.

  - makes life so much more pleasant
  - but not supported in <a href="http://caniuse.com/#feat=css-grid" target="_blank">many older browser versions</a> 
  - but that new <a href="https://www.mozilla.org/en-US/developer/css-grid/" target="_blank">__Firefox grid inspector__</a>! A true <a href="http://www.urbandictionary.com/define.php?term=wowzers" target="_blank">wowzer</a>! 

<br>

### Kaizen method
The <a href="https://en.wikipedia.org/wiki/Kaizen" target="_blank">__Japanese idea and philosophy__</a> of gradual improvement with each iteration. No home runs here, just base hits (_no, I'm not going to use a baseball emoji here, and yes, it's challenging to control my emoji urges_). Iteration after iteration after iteration. Comparable to writing and drafts upon drafts upon drafts, with each getting better.

<br>

### Testing &nbsp; &nbsp; &nbsp; :fire:
__Always__, test, if you can. 

  - But sometimes, yah gottah shoot from dah hips and count your lucky stars.   &nbsp; &nbsp; &nbsp; :star2:__:star2:
  - But today... today, we __test__.

<br>
<br>
<br>

### A Final Note on Grid
I chose to work with the <a href="https://www.mozilla.org/en-US/developer/css-grid/" target="_blank">__grid property__</a> after recently discussing about it and out of curiousity (<a href="https://www.youtube.com/watch?time_continue=48&v=16enLRDbOyY" target="_blank">_great __grid video__ here_</a>). It does make coding, especially with responsiveness, so much more straightforward. However, there is the factor that a page could look really off and, or broken on mobile or tablet view when the property isn't functioning properly, and those views are somewhat a large number (<a href="http://money.cnn.com/2014/02/28/technology/mobile/mobile-apps-internet/index.html" target="_blank">_CNN article: mobile passing desktop_</a>). In the end, I would choose to use it as a development tool but not have it on production, as the number of devices and browsers with inadequate versions to handle this newish css property are too great, in my opinion. Perhaps... I could create a fix for this with JS or one already exists.


<br>
<br>
<br>

## All in all
I hope that last section of the readme wasn't too lengthy or elaborate,
<br> but I wanted to give you a strong sense to how I think, process, and code.  

If you have any questions or comments, feel free
<br> to shoot me <a href="mailto:cucumberandco@gmail.com?subject=Message%20from%20mi-bo%20project">__an email__</a>, and I'll get back to you shortly. 

Cheers. &nbsp;&nbsp;&nbsp; :beers:









