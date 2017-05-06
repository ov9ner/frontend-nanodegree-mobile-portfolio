#Website Performance Optimization portfolio project

    To view the page on a local web server:

$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080

    Open a browser and visit localhost:8080
    Download and install ngrok to make your local server accessible remotely.

$> cd /path/to/your-project-folder
$> ngrok http 8080

    Copy the public URL ngrok gives you and test it through PageSpeed Insights and WebPageTest.


PageSpeed Insights results : (95 / 100) Mobile, (96 / 100) Desktop
### index.html

    converted pizzeria.jpg into 2 images: one 293px width (pizzeria-small.jpg) for the index.html  and one 720px width (pizzeria-medium.jpg) for pizza.html

    Made Google Analytics script asynchronousby adding the attribute async to it.
    added the (media="print") for the stylesheet of print.css


    Removed Google font line because it takes long time to load and is blocking rendering.

    Downloaded thumbnails that are provided after testing with (PageSpeed Insights) and switched them with old unoptimized thumbnails from /img.

    Minified index.html.

    Optimized CSS Delivery



PageSpeed Insights results : (89 / 100) Mobile, (95 / 100) Desktop

### pizza.html


    Work on updatePositions:
    moved "document.body.scrollTop / 1250" out of the for loop

    changed left to transform
    No need to transform 200 pizzas, so get numbers of cols and rows to have the minimum visible requirement.

    Changed querySelectorAll with getElementsByClassName

    Optimized CSS Delivery for style.css for pizza.html

    Minified main.js

