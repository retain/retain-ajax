retain-ajax
===========

[Retain](https://github.com/giuliandrimba/retain) webservice storage plugin

[![Build Status](https://travis-ci.org/giuliandrimba/retain-ajax.png?branch=master)](https://travis-ci.org/giuliandrimba/retain-ajax) [![Coverage Status](http://coveralls.io/repos/giuliandrimba/retain-ajax/badge.png)](https://coveralls.io/r/giuliandrimba/retain-ajax)

### Config

* __url__: REST URL that will be used to save the data.

* __Example:__

  ``` javascript
  var retain = require("retain");
  var retainAjax = require("retain-ajax");
  
  var Movies = retain();
  
  Movies.use(retainAjax, {
        url: "http://localhost:3000/movies"
      })
  ```

### Creating a plugin

[Retain](https://github.com/giuliandrimba/retain) use Promises internally to transfer data between the plugins.

To create a plugin, it is necessary to implement each of the following __Retain__ methods.

* __new__
* __all__
* __set__
* __find__
* __remove__

Each of theses methods must return a promise.

