###PokemonGo-Map Dockerfile
This uses the code located [here](https://github.com/AHAAAAAAA/PokemonGo-Map). It pulls the latest version of the repo and executes the application. 
####Usage
Have Docker installed first. Then:
```
docker pull bkvarda/pokemongo-map-docker
```
To run:
```
docker run -it -p 5000:5000 bkvarda/pokemongo-map-docker -a google -u "your_username" -p "your_password" -l "Some location like Seattle, WA" -st 1000
```
By default this runs on port 5000. Just replace '-p 5000:5000' with -p someport:someport to bind to a different port. Change the other flags as appropriate based on the documentation [here](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Usage).

On Docker for Mac, you may need to add the -H 0.0.0.0 flag at the end like this:
```
docker run -it -p 5000:5000 bkvarda/pokemongo-map-docker -a google -u "your_username" -p "your_password" -l "Some location like Seattle, WA" -st 1000 -H 0.0.0.0
```
To get full list of options, just run the container without any flags like this:
```
docker run bkvarda/pokemongo-map-docker
```
