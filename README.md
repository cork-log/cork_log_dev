# Docker Composition for Cork-Log
This repo is just here to ease development for this project.

## Running
1. Clone down the repo 
2. Run the init script to sync up the nested submodules.
	```
	$ ./init-repo.sh
	```
3. The entire environment will spin up with:
	```
	$ docker-compose up
	```
## Developing
When developing, it is usually easier to let docker compose manage all services that you aren't currently developing in, and then running the one you are developing locally.\
For example,
```
$ docker-compose up gateway mongodb
```
will spin up just mongo and gateway in docker, but since docker exposes their services to the host machine, the `handy_api` can be worked on very easily.