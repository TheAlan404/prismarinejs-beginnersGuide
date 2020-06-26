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
