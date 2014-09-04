MendeleyJS
==========

a small node module to mediate requests and client credentials auth to the mendeley api 
Javascript + Mendeley Public API
============

note : im still writing this

A wrapper for the mendeley api's public methods, compliant with the new oauth 2.0 implementation.

###Supported Methods
<pre>auth("clientid", "client secret", resultHandler)
search("searchterm", resultHandler)</pre>

###Inclusion
```javascript
npm install mendeleyjs
```

```javascript
var Mendeley = require('mendeleyjs');
```

###Usage

create an instance of the library

```javascript
Mendeley.auth('clientID', 'client secret', function(msg) {
    console.log(msg)
    Mendeley.search("science", function(data) {
        console.log(data);
    });
});
```

###About

[Mendeley](http://www.mendeley.com/) is a site that provides tools to manage references and citations to academic research papers. They also provide a search facility for their paper collection. This wrapper is being developed to link Mendeley into the search feature of [Seeder](https://github.com/ammanvedi/seeder)

I will be adding more methods to the api soon.
