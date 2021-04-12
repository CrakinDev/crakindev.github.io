---
layout: posts
title: Enhancement One
---

## Project
---
[Xandrion Discord Bot](https://github.com/CrakinDev/xandrion2-bot)

## Artifact
---
The artifact for this enhancement category is a simple Discord bot. The basic version of it was created just before and into Week 1 of the Capstone course in preparation for using it to demonstrate proficiencies and learned concepts. Also, it was chosen as it could integrate very well into a Full Stack application if using the DiscordJS Node module.

The artifact was chosen as part of the portfolio because it can be a strong standalone application. By itself, it has all the necessary commands and access to data to relay useful information back to the user about their in-game activities. However, as part of a larger application it becomes a useful tool in quickly accessing shared information without having to access the dashboard site.

The specific components that showcase my abilities are two-fold. The first is how quickly the standalone application can be setup with basic functionality and deployed. Many times, speed and timing of deployment are paramount even if not yet fully featured. The second is still in progress but is the ability to link like-minded applications to a greater project. The amount of data available from the game API is immense and without proper data handling and useful processing, display of that data would still be just as confusing to a user as raw JSON to a non-developer.

## Improvements
---
The command structure outlined in the code review was revised to use some common properties to allow all commands needed access to parameters and parsing to use a common algorithm. Users are able to use the !last command and can specify a game activity type and number of activities to retrieve.

Example:
```
!last 5 strikes
```
Returns averages from the last 5 strike activities.

Users are also able to register to the bot utilizing the ```!registerme``` command. This command also takes parameters of a username and a platform (ex: ```!registerme Crakin Xbox```). This is required to lookup the user profile on the Bungie API and return a membership ID. The membership ID can then be used to look up the character IDs associated with the account and then access activity statistics. Registration allows the bot to associate a Discord Account ID with the game membership ID/character IDs. This data is kept in the MongoDB database instance.

The database instance was setup and used lightly with the bot. A User collection stores a Discord ID and associated game membership and character IDs that were looked up during registration. This provides two key improvements: (1) the user does not have to specify their username and platform when issuing commands that retrieve stats and (2) the bot does not have to query the API for membership ID or character ID lookup. This improves lookup time and reduces API queries lessening the chance the bot or backend lookup gets throttled.

## Objectives
---
All intended objectives were met. This particular artifact was meant to be a standalone data accessor as part of a larger project that interfaces with Discord instead, but not in place of a website dashboard. As the local backend API server evolves, there may be some further updates to the bot to accommodate those or some slight database schema changes, but nothing major.
 
## Reflection
---
The Discord bot aspect of this project is the easiest part of the entire application. While the entire Node module was new to me ([DiscordJS](https://github.com/discordjs/discord.js/)), Node-based applications are not. The most “treacherous” part of web-based applications is asynchronous code. It can, and usually does, turn into an absolute mess so navigating the logic cleanly is essential. In this project, there’s a fair bit of Promise usage mainly in backend API calls and game API calls. Database read/writes also require Promise callbacks. Handling these cleanly and keeping proper track of scope while writing callbacks is something I’d like to master. This project has allowed me to explore greater usage of these types of logic within inter-connected applications where performance is key.


