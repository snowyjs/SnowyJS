# SnowyJS, snowy.js is a package that make it possible to startup a nodejs ( discord.js ) project within a few seconds.

# TypeScript / NodeJS / Discord.js Usage:
```js
const { botready, snowyjs, ping, math } = require("snowyjs");
const discord = require("discord.js");
const fs = require("fs");
const ms = require("ms")

const bot = new discord.Client();

bot.on("ready", () => {
  botready();
  snowyjs();
});)

bot.on('message', msg => {
  if (msg.content === 'ping') {
    msg.reply('pong');
    ping();
  }
});

bot.on('message', msg => {
  if (msg.content === 'math') {
      var answer = math(args[0], args[1])
    msg.reply(answer);
  }
});

bot.login('BOT TOKEN HERE');
