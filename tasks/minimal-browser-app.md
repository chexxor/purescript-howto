# Minimal Browser App

How to make a minimal PureScript browser app.
 
## Prerequisites

  * Node & npm
  * Bower
  * PureScript tools available on `$PATH`

## Initialize a PureScript project

``` bash
$ mkdir ~/foo; cd ~/foo
$ pulp init
$ pulp run
Hello sailor!
```

## Build and bundle to run in browser

Compile the PureScript modules into JavaScript modules, then bundle them into a single file, as browsers can't load modules (i.e. `require`).

``` bash
$ mkdir dist
$ pulp build
$ purs bundle output/**/*.js -m Main > dist/app.js
# The `-m` flag specifies the top-level module. Only transitively referenced
#   functions are included in the output (DCE). Note that we _do not_ use the
#  `--main` flag, which will execute the `main` function in the top-level module
#  when the JavaScript file is laoded. For this example, we want to use this
#  function as a library, not an executable.
```

## Execute app in JavaScript script tag

Build an HTML page which executes the app by executing its entrypoint, the `Main.main` function, in a script tag.

``` bash
$ mkdir dist
$ $EDITOR dist/index.html
```

Paste the following HTML into `dist/index.html`.

``` html
<!DOCTYPE html>
<html lang="en">
 <head>
     <meta charset="UTF-8">
 </head>
 <body>
     <script src="app.js" charset="utf-8"></script>
     <script>
       document.addEventListener('DOMContentLoaded', function () {
           PS.Main.main();
       });
     </script>
  </body>
 </html>
```

## Serve and execute the browser app

``` bash
# In a new console session:
$ cd dist
$ python -m SimpleHTTPServer
# Open http://localhost:8000 in your browser.
# Open JavaScript console and reload the page.
# See "Hello, sailor!" in the JS console.
```

## Alternative ways of running the app
 
In a browser's JavaScript console.

``` javascript
# Open a JavaScript console in the browser window used to open http://localhost:8000
> PS.Main.main()
# Note that if `Main.main` accepts arguments, you will need to pass them as
#   multiple function invocations `PS.Main.otherfunc(p1)(p2)`, as PureScript
#   curries all functions by default.
```

In an OS console. You can run the unbundled copy of the browser app in a REPL. This will fail if the app uses APIs not available in NodeJS, such as DOM APIs.

``` bash
$ pulp repl
> import Main
> main
"Hello, sailor!"
$ node
> var Main = require('./output/Main');
> Main.main()
Hello, sailor!
{}
```
