# HW 1: Game List!

Follow these steps to get your project ready to work on:

1. clone this repo to your development machine
3. cd into the new directory (e.g., `$ cd hw-1-game-list-numerator`)
3. run `npm install` in the project directory (this will install all of the packages listed in package.json)
4. run `npm start` to make sure everything is set up correctly
5. start working on your project

## Assignment Overview
This assignment is intended to give you practice using ExpressJS fundamentals, including routes, routers, and middleware.

You will build a server that allows a client to create, read, update, and delete listings of video games. There will be two separate collections, each managed by a different top level route:
* `/mobile` will manage a list of mobile games
* `/desktop` will manage a list of desktop games

For testing purposes, you can find lists and info about (mobile games) [https://en.wikipedia.org/wiki/Category:Mobile_games_by_platform], as well as for (desktop games) [https://en.wikipedia.org/wiki/List_of_PC_games_(A)]. Seed data, with examples showing the supported data structure for each list, is provided in the `data` directory. You should not modify the files in that directory.

Since it assumed that mobile game users will access the site from a mobile app, the `/mobile` route will only accept data in JSON format and will provide data in JSON as well. Desktop users are assumed to access the site using a web browser, so the `/desktop` route will accept only HTML form data and will provide data in plain text. 

For each route, your server must provide the following capabilities to the client:
* provide a list of all games
* provide details of a particular game using its ID
* add a new game to the list
* modify details of a game
* delete a game

Additional details/requirements:
* For legacy reasons, the mobile games list uses only numerical IDs and the desktop games list uses strings. Ensure that invalid IDs result in informative errors.
* adding, modifying, and deleting games are only allowed for clients that include the Authorization header with "Bearer SI679HW1"

### Grading (up to 120 points)
| No. | Requirement  | Points |
| --- | ------------- | ------------- |
| 1 | Solution uses Routers effectively to manage the two lists independently | 20  |
| 2 | Appropriate HTTP methods/verbs are used for each operation | 20 |
| 3 | Data validation for ids is handled by middleware and returns appropriate status codes and error messages for both valid and invalid inputs  | 20 |
| 4 | Protected routes are correctly protected using middleware and appropriate status codes and error messages are returned for both allowed and prevented attempts | 20 |
| 5 | Fall-through handling of errors is included for errors not explicitly handled | 10 |
| 6 | Code style is good: naming, structure, formatting, etc. align with professional norms  | 10 |


## Extra credit (Up to 4 points):
If you want some extra challenge (and points!) you can add a few other features to your server.

### Grading
| No. | Requirement  | Points |
| --- | ------------- | ------------- |
| X1 | Add a top level route with an appropriate name that always returns an HTTP 418 error | 1 |
| X2 | Add the ability to filter the games that are shown using query strings. One point for each filtering option supported. You must document your filtering options in your Canvas submission. | 3 |

| | **Total** | **4**

### Submitting your work
Push your code to your repo before the deadline. Also submit a link to your repo via Canvas along with any comments that could help us grade your assignment(e.g. whether or not you did the extra credit, things that don't quite work but you want to argue for partial credit).
