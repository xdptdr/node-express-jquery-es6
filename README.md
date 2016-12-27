# node-express-jquery-es6
Kickstart serving your static bundled transpiled content

You've been told, Node.JS is cool.

You've discovered that Node.JS doesn't provide anything to serve static files, and that you may use [express](https://www.tutorialspoint.com/nodejs/nodejs_express_framework.htm).

You've discovered NPM and modules and that [ES6 modules are a work in progress](http://exploringjs.com/es6/ch_modules.html#sec_module-loader-api), but in the meantime, you may use [browserify](http://browserify.org/).

You've discovered that ES6 itself is a [work in progress](https://kangax.github.io/compat-table/es6/), although [the standard was finalized in June 2015](https://en.wikipedia.org/wiki/ECMAScript#6th_Edition_-_ECMAScript_2015), and that in the meantime, you may use [babel](https://babeljs.io/).

And now you're sitting there with your application script, your [jQuery](https://jquery.com/) script, and you're feeling lost. Then don't panic, and fork this project.

## What's in there

This project contains a minimalist script that requires jQuery from NPM. The scripts are bundled with browserify and transpiled with babel. The content is served statically with the express framework.

## Usage

```
npm install
npm install -g browserify watchify
```

Then, in one terminal:
```
watchify -d app\app.js -t babelify -o public\app.js
```

In another terminal:
```
node server.js
```

In a browser:
```
localhost:8081
```

Shorthand provided scripts in package.json:
```
npm run bundle
npm run watch
```