# Docker compose.

If you have started working with Docker and are building container images for your application services, you most likely have noticed that after a while you may end up writing long `docker container run` commands.
These commands while very intuitive can become cumbersome to write, especially if you are developing a multi-container applications and spinning up containers quickly.
Docker Compose is a “*tool for defining and running your multi-container Docker applications*”.
Your applications can be defined in a YAML file where all the options that you used in `docker container run` are now defined.
Compose also allows you to manage your application as a single entity rather than dealing with individual containers.

## Terminology
- *docker-compose.yml* The YAML file where all your configuration of your docker containers go.
- *docker-compose* The cli tool that enables you to define and run multi-container applications with Docker
  - *run* :
  - *up* : creates and starts the services stated in the compose file
  - *down* : stops and removes containers, networks, images, and volumes
  - *restart* :
  - *logs* : streams the acummulated logs from all the containers in the compose file
  - *ps* : same as pure `docker` variant; shows you all containers that are currently running.
  - *rm* : removes all the containers from the given compose file.
  - *start* : starts the services
  - *stop* : stops the services

The docker cli is used when managing individual containers on a docker engine.
It is the client command line to access the docker daemon api.

The docker-compose cli can be used to manage a multi-container application.
It also moves many of the options you would enter on the docker container run cli into the docker-compose.yml file for easier reuse.
It works as a front end "script" on top of the same docker api used by docker, so you can do everything docker-compose does with docker commands and a lot of shell scripting.



* Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.
* Lastly, run docker-compose up and Compose will start and run your entire app.
