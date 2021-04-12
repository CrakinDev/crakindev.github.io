---
layout: single
title: Enhancement Two
categories: 
  - enhancement
---

## Project
---
[Xandrion Data API](https://github.com/CrakinDev/xandrion2-api)

## Artifact
---
The artifact for this enhancement category is an Express-based NodeJS API server. Its purpose is to be a one-stop shop for both the Discord bot and web Dashboard’s to source data. This ensures the data is centrally located and both applications use and handle the same data through common accessing means.

The initial creation was just after the Discord bot during week 1 of the term. It was setup as a working listening server, but without any useful developed endpoints or database accessing logic. It was simply a bare server setup as a boilerplate that would start-up, listen and respond to a single endpoint with just a generic “Hello World” response.

## Improvements
---
The improvements made were the development of the 3 main endpoints the applications would utilize: auth, register, and activities.
The auth endpoint will be the redirect source for the dashboard checking if the required information is present for the current user. If not, we will proceed to the registration page and if so, will continue to the main dashboard page. This endpoint is very simple and also exists so that the user will not have to login each and every time they visit the dashboard. The Express-Sessions node module saves the user session via cookie and an entry in the Mongo database so that they will automatically be redirected to the dashboard with a valid session still stored.

The registration endpoint is to gather the required information from the user (Discord ID) and associate it with a specific game account ID (Bungie Membership ID) and associated characters on the account (Character IDs). This way, we do not have to ask the user for their own account information every time they visit the dashboard or place a command to the Discord bot. This endpoint takes 3 parameters: one from the endpoint URL and two supplied in the request. The endpoint (/register/<discordID>) supplies the Discord ID in the url and the game account name and platform in the request itself as it will be form data from the dashboard or gathered message data from the Discord bot. The endpoint will then lookup the account using the specified information and write the results (with fail-safe logic!) to the Mongo database. Thus, the Discord ID will always be associated with the found account data throughout all data fetching procedures.
	
Lastly, the activities endpoint was created. This activity uses the associated account data to lookup activity results from the type specified (i.e., Strikes, Crucible, etc. – in-game terms). The Bungie API provides this data very easily so long as you have the required data. This endpoint will use the “GetActivityHistory” Bungie API endpoint to fetch useful data pertaining to all characters (up to 3) on a player account. This endpoint will also parse through the JSON response and create a processed array. This array contains all the stats of the activities and sheds much of the extra data the application will not use. Finally, the array is processed as a strinified JSON object and sent as the response. The front-facing application will then use this response data as it sees fit.
 
## Objectives
---
All initial objectives were met, however, the Dashboard may require some extra data from the Bungie API to display character names, emblems, equipped items, etc. This can either be done from the dashboard directly, or, to keep things all in one place, can become its own “aesthetic” endpoint. For now, the useful data objects have been met and can be used to complete the functional side of the overall application.
 
## Reflection
---
I was amazed at how easy it was to setup a very basic API server and distribute data. Using this method across applications with similar goals will be exceptionally helpful to my future developments. Furthermore, small, custom, encapsulated local servers could be helpful to my work projects. We are starting to delve into multiplayer capable applications. While that is mostly handled by the game engine itself, aggregate data and analytics are ultimately what clients are usually after. This data would be individually logged to a database from each client machine. However, using an API for both accessing and ingestion, would streamline the process and make development much easier as the API would act as an interface. The client machines would merely access the endpoint and POST their data, while applications would access from GET endpoints. The API would handle all the required processing itself centrally.


