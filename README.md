# PHP MVC Starter

This repo contains a super simple architecture for a PHP website using a MVC paradigm.

# Lifecycle

- User requests the home of the website
- index.php replies redirecting to /home
- /home is picked up by .htaccess and gets redirected to /controlles/home.php
- the controller 
    - grabs any payload, executes it's logic through its data model stored in /models/home.php
    - instantiates the templating engine
    - creates data that gets passed over to the view
- the view
    - the view at /views/home.php extends views/mainlayout.php
    - mainlayout is the entire layout of the page, from <pre>html</pre> to <pre>/html</pre>
    - this file has pre-defined spots where data will get inserted
    - the view at /views/home.php gets the data sent by the controller and starts assembling it as HTML
    - HTML is assigned to "blocks" which are then replaced on the mainlayout template