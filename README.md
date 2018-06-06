Welcome to the example task from IMPARGO. If please read these instructions
carefully. If you have any questions please write me an e-mail at
j.labeit@impargo.de.

# Overview
The task is about building a web application for users who want to find a gas
station in Berlin. The final goal is that a user can click on a map and the
application shows the name of the nearest gas station and the location of the
gas station on a map. The web-application has two parts.
 - The client (in `client`) which is a react application showing the map.
 - The server (in `server`) which is a nodejs server which is used to find the
   nearest gas station.

# Getting started
Before you start you should have a recent version of `npm` and `node`
installed.
To start the server go into `server` directory and run
```
  npm install
  node index.js
```
To see if the server work check localhost:3000 and see if you get a json object
with information about a gas station.

To build the client go into the directory `client` and run
```
npm install
npm run start
```
Then open the file `client/dist/index.hmtl` in the browser. (Make sure that the
server is still running! You should now see a welcome message, the name of the
first fuel station `Aral` and an empty map of Berlin.

# Task 1 - Display gas station on map (client)
In the first task display the location of the first gas station on the map. The
map uses the leaflet library.  Use a marker and position it on the map
(checkout https://leafletjs.com/ for details).

# Task 2 - Get coordinates of map click (client)
When the user clicks on the map capture this event and convert the click into
geocoordinates (lat and lon). When the users clicks make a request to the
server to get the nearest fuel station. Change the fetch request to the server
to include these coordinates as query string. E.g.
`localhost:3000?lat=42.1&12.1`.

# Task 3 - Get nearest gas station (server)
Change the server so that it can receive the previously sent coordinates.
Instead of returning the first gas station the server should return the closest
gas station to the sent coordinates.

# Extra Task - Display distance + design (client and server)
If you want to you can additionally change the server so that it also return
the distance (in meters) to the nearest gas station. Then show the distance in
the front-end. If you want to you can additionally add more styling to the
application in `client/dist/styles.css`.


