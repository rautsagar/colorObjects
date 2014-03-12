Programming problem
-------------------
 
Retrieve and render a collection of objects from a server, handle state transitions

Using languages, frameworks and tools of your choice, implement the following:

    A web service that exposes a REST interface, and allows the client to retrieve a collection of objects.
        Each object has the following attributes: id, and 'color'. Color can be one of red, green or blue.

    A client UI that:
        Retrieves the collection of objects from the web service
        Displays objects while grouping them based on the associated color
        Allows the user to reassign any object to a different color

Solution
--------
The REST API is made using Node.js and express.js.
    The code for the API is locates in /app.js

The user Interface is made using Jade template, and is located in the file /views/index.jade
    The stylesheet is defined in the file /public/stylesheets/custom.css

 
The MV* framework used in the fronted is Backbone.js
The ability to reassign the objects to different groups dynamically calls for storing the data in models linked to views, hence I used backbone.
    All the Javascript/backbone functions defined by me are located in /public/stylesheets/functions.js

Files
-----

The root page for the web server is located at:

    views/
        index.jade

More about Jade: [here](http://jade-lang.com/)

The css and JS files are located in:

    public/
        stylesheets/
        javascripts/


API
---

This solution is packaged with a simple nodejs/express app provides the following API:

    GET /api/objects
        - returns an array of 'objects' in the format:
            {
    			"id": 1,
    			"color": "green"
  			}

Setup
-----

In order to test, you'll need to install [nodejs](http://nodejs.org/) if you don't have
it already. You should then follow these steps:

Extract the tarball and enter the extracted directory:

    $ tar xzvf colorObjects.tar.gz
    $ cd colorObjects

Install the npm dependencies

    $ npm install

Run the app

    $ node app

You can then view the server on your machine at port 3000 in your browser.