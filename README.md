
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