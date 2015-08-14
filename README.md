Silex Template
========
Welcome to Silex Template, a functional Silex application that you can use as template for your new applications.

This document contains information on how to start using the Silex Template.

Creating a Silex Application
----------------------------

Silex uses [Composer](http://getcomposer.org/) to easy creation of a new project:

```sh
$ git clone https://github.com/nicorivas07/silex-template.git
$ cd silex-template
$ sudo composer-update
```
Composer will create a new Silex project under the path/to/install directory.

Browsing the Hello World Demo
-----------------------------
```sh
$ cd path/to/install
$ composer run
```
Then, browse to http://localhost:8888/

Also you can try http://localhost:8888/your_name

Application structure
---------------------

    - app
      -- config - Contains the dev.php and prod.php files with configuration data (db credentials, etc).
      -- app.php - Called by index.php, initializes the app by registering libraries into the dependency injection container.
      -- routes.php - Called by index.php, routes map urls to controller classes.
    - src - Contains the main application code
      -- AppName - this folder contains the root of the namespace. All classes are nested below.
        --- Controller - Contains the controller classes.
        --- Entity - Contains the entities.
        --- Repository - Contains classes that manipulate entity data by doing queries against the database. This includes all CRUD operations.
    - vendor - Contains the dependencies managed by composer.
    - web - Contains static files (CSS, JS, etc) as well as the main entrypoint (index.php)