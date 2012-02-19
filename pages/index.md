# Hello World

by [@twilson63](http://twitter.com/twilson63)

posted 2012-02-18

## Introduction

A nodejs and coffeescript hello world tutorial.

## Requirements

[nodejs](http://nodejs.org)

## Install CoffeeScript

``` sh
npm install coffee-script -g
```

## Code

Lets go ahead and create our first web server using nodejs and coffeescript.

In your favorite text editor type the following:

``` coffeescript
http = require 'http'

server = http.createServer (request, response) ->
  response.writeHead 200, 'Content-Type: text/plain'
  response.end 'Hello World'

server.listen 3000, console.log 'listening on 3000...'
```

Save the file as server.coffee.

Open a command prompt in the directory that the server.coffee file is in.

Run the following:

``` sh
coffee server.coffee
```

You should see the prompt return "listening on 3000...", now you should be able to open a browser at 'http://localhost:3000' and see 'Hello World'.

Congratulations! You just created your first nodejs web server.

Press CTRL-C in the command window to stop the server.

## Compile the server

Lets compile your coffeescript into javascript.

In the command window we will execute the coffee command we did previously, but this time we will add a -c flag to tell coffeescript to compile the coffee file to a javascript file.

``` sh
coffee -c server.coffee
```

This will create a new file in the same directory called 'server.js'.  You can open server.js and you should see the generated javascript like this.

``` javascript
var http, server;

http = require('http');

server = http.createServer(function(request, response) {
  response.writeHead(200, 'Content-Type: text/plain');
  return response.end('Hello World');
});

server.listen(3000, console.log('listening on 3000...'));
```
