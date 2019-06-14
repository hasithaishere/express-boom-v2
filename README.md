# express-boom-v2

[Boom](https://www.npmjs.org/package/boom) response objects in Express.


This plugin forked from the [scottcorgan/express-boom](https://github.com/scottcorgan/express-boom) ( *NPM module:* [express-boom](https://www.npmjs.com/package/express-boom) ) and update the previous deprecated [boom](https://www.npmjs.com/package/boom) dependency to new [@hapi/boom](https://www.npmjs.com/package/@hapi/boom) module.

All credits goes to **Scott Corgan** and team.

## Install

```
npm install express-boom-v2 --save
```

## Usage

```js
var express = require('express');
var boom = require('express-boom-v2');

var app = express();

app.use(boom());

app.use(function (req, res) {
  res.boom.notFound(); // Responds with a 404 status code
});

app.use(function (req, res) {
  // some validation check fail and returns an object : reasons
  
  res.boom.badRequest("Validation didn't suceed", reasons); // Responds Boom message + reasons object
});

app.listen(4444);
```

For a complete list of methods, see the [Boom docs](https://github.com/hapijs/boom#overview)
