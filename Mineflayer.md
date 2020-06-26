Mineflayer Begginers Guide
==========================

Welcome to the begginers guide for Mineflayer!
Mineflayer is an API that can be used for making minecraft bots.

Creating your first bot
-----------------------

To make a bot, make sure mineflayer is installed.

<TODO: add link to project.md>

First, we need to make sure NodeJS loads mineflayer.
```js
const mineflayer = require("mineflayer");
```

After that, we can add the function that creates the bot.
```js
var bot = mineflayer.createBot({
  host: "localhost",
  port: 25565,
  username: "email@example.com",
  password: "12345678",
  version: false
});
```
The `host` is the server IP. `port` is the server port.

If you want to make a bot that connects to a cracked server, leave out the `password` part and type the username to `username`.
If the bot is not connecting to a cracked server, type the email into `username`.

The `version` is the version of mineraft that the bot will connect. If you enter `false`, the bot will guess the server version.
If you want to define the version, replace the `false` value with the server version. (Version must be a string)

If you start your NodeJS app, you would see that the bot connects to the server, how cool?

Using Bot Events
----------------

Events are functions that run when something happens, for example lets look for chat messages.
```js
bot.on("event name", function(arg1, arg2){
  //Code that will be run
});
```
Events are like as seen above, you put the event name to `event name` and the arguments to `arg1, arg2`.

Another example: reply to people that say "Hi"
```js
//      Chat event       v Has 2 arguments
bot.on("chat", function(username, message){
  if(message == "Hi") {
    bot.chat("Hello!"); //Bot sends a chat message!
  }
});
```

How to use the docs
-------------------
<TODO: link to mineflayer docs>

You can see that the API documentation has a table of contents.
You can just scroll to the "Bot" section, all the things above it like `mineflayer.furnace` is more advanced.

Events are events like seen above.

Functions returns values so you can save them as varailables like
```js
var myBlock = bot.blockAt(point);
```

Methods are just functions that return nothing. They do stuff.

Properties are values, you can save them like methods. Most of them are read-only so changing them may break the bot.

`point` is a vec3 class.
You can install and use it with `npm`

<todo: npm and vec3 link>






















