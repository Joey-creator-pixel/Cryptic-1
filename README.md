# Cryptic
A fully customizable bot built with discord.js


<h1 align="center">
  <br>
  <a href="https://github.com/romanbeard112/Cryptic"></a>
  <br>
  Cryptic
  <br>
</h1>

<h3 align=center>A fully customizable bot built with <a href=https://github.com/discordjs/discord.js>discord.js</a></h3>


<div align=center>

  <a href="https://discord.gg/DFZv2Zh">
    <img src="https://discordapp.com/api/guilds/705344500507345017/widget.png?style=shield" alt="shield.png">
  </a>

  <a href="https://github.com/discordjs">
    <img src="https://img.shields.io/badge/discord.js-v12.3.1-blue.svg?logo=npm" alt="shield.png">
  </a>

  <a href="https://github.com/romanbeard112/Cryptic/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-GNU%20GPL%20v3-green" alt="shield.png">
  </a>

</div>

<p align="center">
  <a href="#about">About</a>
  •
  <a href="#features">Features</a>
  •
  <a href="#installation">Installation</a>
  •
  <a href="#setting-up">Setting Up</a>
  •
  <a href="#license">License</a>
</p>

## About

Cryptic is an open source, fully customizable Discord bot that is constantly growing. It comes packed with a variety of commands and a multitude of settings that can be tailored to your server's specific needs. Cryptic's codebase also serves as a base framework to easily create Discord bots of all kinds. You can invite Cryptic to your Discord server using [this link](https://discordapp.com/oauth2/authorize?client_id=612134650114080818&scope=bot&permissions=403008599)! Also, you can join our official [Support Server](https://discord.gg/DFZv2Zh) for all questions, suggestions, and assistance!

If you liked this repository, feel free to leave a star ⭐ to help promote Cryptic!

## Features

**110+** commands and counting across **8** different categories!

  * **Administration:** A huge amount of settings to customize with commands like `setprefix`, `setwelcomemessage`, and `setverificationrole`.
  * **Moderation:** Commands such as `kick`, `ban`, and `mute` to assist your moderation staff.
  * **Fun & Games:** Tons of fun commands like `trivia`, `meme`, `emojify`, and a variety of animal pic commands like `cat`, `dog`, and `fox`.
  * **Information:** Commands like `userinfo` and `serverinfo` for general utility.
  * **Points:** A unique points system with a rotating winner that has commands like `leaderboard`, `givepoints`, and `crown`.
  * **Color:** Change your Discord color with commands like `color`, `createcolor` and `randomcolor`.
  * **Bot Owner:** Owner specific commands like `eval` and `servers`.
  * **Miscellaneous:** All other commands like `feedback` and `bugreport`.

Cryptic also comes with a variety of features, such as:

  * **Auto role** assignment.
  * Server **verification** via reactions.
  * **Welcome messages** and **farewell messages**.
  * **Logging** for mod commands and various events.
  * A **Moderator only** channels.
  * A **starboard** system.
  * An **Auto kicking** system, when a warn limit is reached.
  * Automates **random colors** when members join.
  * Per **command disabling** system.
  * And much more! There are over **30+** settings to tweak!


## Installation

You can add Cryptic to your server with [this link](https://discordapp.com/oauth2/authorize?client_id=612134650114080818&scope=bot&permissions=403008599)! Alternatively, you can clone this repo and host the bot yourself.
```
git clone https://github.com/romanbeard112/Cryptic.git
```
After cloning, run an
```
npm install
```
to snag all of the dependencies. Of course, you need [node](https://nodejs.org/en/) installed. I also strongly recommend [nodemon](https://www.npmjs.com/package/nodemon) as it makes testing *much* easier.

## Setting Up

You have to create a `config.json` file in order to run the bot (you can use the example file provided as a base). Your file should look something like this:
```
{
  "token": "your_token_here",
  "ownerId": "your_ID_here",
  "bugReportChannelId": "bug_report_channel_ID_here",
  "feedbackChannelId": "feedback_channel_ID_here",
  "serverLogId": "server_log_ID_here",
  "apiKeys": {
    "catApi": "your_API_key_here",
    "googleApi": "your_API_key_here"
  }
}
```
Visit the Discord [developer portal](https://discordapp.com/developers/applications/) to create an app and use the client token you are given for the `token` option. `ownerId` is your own Discord Snowflake. `bugReportChannelId`, `feedbackChannelId`, and `serverLogId` should be set to the respective text channels on your own server. To get keys for supported APIs, vist:

  * [TheCatAPI](https://thecatapi.com/)
  * [Google APIs](https://console.developers.google.com/apis/)

After your `config.json` file is built, you have enable `Privileged Intents` on your Discord [developer portal](https://discordapp.com/developers/applications/). You can find these intents under the "Bot" section, and there are two ticks you have to switch on. For more information on Gateway Intents, check out [this link](https://discordjs.guide/popular-topics/intents.html#the-intents-bit-field-wrapper).

Once done, feel free to launch Cryptic using the command `node app.js` or `nodemon app.js`. If on Linux, you can also kick off using the `start.sh` script. If you need additional help setting up, join our [Support Server](https://discord.gg/DFZv2Zh)!

**Important Note:** Do not use Heroku to host Cryptic! Cryptic uses SQLite as its database which backs up its data store on disk. Heroku clears its content often, so your database will be wiped. [READ MORE HERE](https://devcenter.heroku.com/articles/sqlite3).

### Emojis

If you are **self-hosting** Cryptic, you may notice that the emojis for certain commands are not displaying. This is because Cryptic uses **custom emojis** for a variety of its commands. These emojis will have to be added to your own server, and you will have to change the corresponding IDs in the `emojis.json` util if you would like to use them. Or, you can replace the emojis in `emojis.json` with ones you already have access to. If you would like to use Cryptic's original custom emojis, hop into our [Support Server](https://discord.gg/DFZv2Zh) where you can snag them all.

### Colors

Upon being invited to a server, Cryptic will automatically create **6** predefined colors for your server to enjoy. To add more, use the provided `createcolor` command to quickly and easily create new colors.

To add colors manually, first create a few empty roles at the bottom of your server's role hierarchy. The names of these roles must begin with the character `#`, for example, `#Red` or `#Blue`. Then change the color of that role to your desired hex, and that's it! After they are set up, the members of your server can then change their color by using Calypso's color commands!

## License

Released under the [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html) license.

## To-Do

Cryptic is in a continuous state of development. New features/updates may come at any time. Some pending ideas are:

  * Music
  * Automod
  * Stream alerts
  * Custom tag/reaction system
