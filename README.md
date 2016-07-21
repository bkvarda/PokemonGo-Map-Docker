###PokemonGo-Map Dockerfile
This uses the code located [here](https://github.com/AHAAAAAAA/PokemonGo-Map). It pulls the latest version of the repo and executes the application. 
####Usage
Have Docker installed first. Then:
```
docker pull bkvarda/pokemongo-map-docker
```
To run:
```
docker run -P pokemongo-map-docker -a google -u "your_username" -p "your_password" -l "Some location like Seattle, WA" -st 1000 -H 0.0.0.0
```
By default this runs on port 5000. Just replace '-P' with -p someport:someport to bind to a different port. Change the other flags as appropriate based on the documentation [here](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Usage). On Docker for Mac, we need to bind to 0.0.0.0 in order to reach using http://localhost:5000 (thus, the flag -H 0.0.0.0).


