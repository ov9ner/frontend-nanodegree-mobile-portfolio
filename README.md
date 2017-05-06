#Website Performance Optimization portfolio project

    To view the page on a local web server:

$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080

    Open a browser and visit localhost:8080
    Download and install ngrok to make your local server accessible remotely.

$> cd /path/to/your-project-folder
$> ngrok http 8080

    Copy the public URL ngrok gives you and test it through PageSpeed Insights and WebPageTest.


### index.html

    converted pizzeria.jpg into 2 images: one 293px width (pizzeria-small.jpg) for the index.html  and one 720px width (pizzeria-medium.jpg) for pizza.html

    Made Google Analytics script asynchronousby adding the attribute async to it.
    added the (media="print") for the stylesheet of print.css


    Removed Google font line because it takes long time to load and is blocking rendering.

    Downloaded thumbnails that are provided after testing with (PageSpeed Insights) and switched them with old unoptimized thumbnails from /img.

    Minified index.html.

    Minified HTML

###Results: PageSpeed Mobile: 94 PageSpeed Desktop: 91 Webpagetest 3G: fully Loaded 2.3s

##pizza.html ###Starting point (from source): 2015-12-13 17:06:17.681 main.js:494 Average time to generate last 10 frames: 49.501000000000204ms 2015-12-13 17:06:18.444 main.js:494 Average time to generate last 10 frames: 46.564500000000045ms 2015-12-13 17:06:20.018 main.js:466 Time to resize pizzas: 113.5649999999996ms 2015-12-13 17:06:21.284 main.js:466 Time to resize pizzas: 113.5649999999996ms

    Optimise pizzeria images, serving 2 versions media queries.
    Work on updatePositions:
    moved "document.body.scrollTop / 1250" out of the for loop
    added will-change: transform; to .main in style.css
    changed left to transformX
    No need to transform 200 pizzas, so get numbers of cols and rows to have the minimum visible requirement.
    Resize pizza, no need to calc dx & newwidth in the for loop, all same size so getting these from [0] is enough
    changed querySelectorAll with getElementsByClassName
    got size of array before loop

###Results: 2015-12-14 21:24:04.349 main.js:523 Average time to generate last 10 frames: 0.29600000000000365ms 2015-12-14 21:24:04.516 main.js:523 Average time to generate last 10 frames: 0.3085000000001855ms 2015-12-14 21:24:07.908 main.js:495 Time to resize pizzas: 1.4599999999991269ms 2015-12-14 21:24:09.894 main.js:495 Time to resize pizzas: 1.4599999999991269ms 2015-12-14 21:24:12.669 main.js:523 Average time to generate last 10 frames: 0.2565000000002328ms

#TO DO:

    See if using web workers for some of the functions would help performaances
    There are no timer but maybe it would be possible to implement requestAnimationFrame
    Improve the design of the pizzeria page, lots to be done here

