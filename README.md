# VENoM-Docker
Vue, Express, Node, Mongo with Docker-compose setup for local development. Hot Reload, SASS live compilation, among other goodies :)  

Tutorial here:

https://medium.com/@audretschjames/venom-stack-docker-setup-for-local-development-457093761ad1

### Steps to Run

1. Clone this repository

> git clone https://github.com/jamesaud/VENoM-Docker

2. Navigate into the directory VENoM-Docker

> cd your-path-to/VENOM-Docker

3. Build Docker Images

> docker-compose build

4. Run the stack :)

> docker-compose up

Your app should be running on (if using native docker).: 

http://localhost:8080

Be patient and wait for all for all of the NPM warnings to finish - this will only happen once. Happy developing! 


### Configuration

There are 3 parts to this dockerized Vue app: Frontend (Vue), Backend (Node with Express), and Database (MongoDB).

The frontend is in the 'client' folder, backend in the 'server' folder, and the database is mounted to your current directory in the 'db' folder. 

NPM apps are a bit tricky to install in Docker, because the binaries have to be installed in the container. Though there are several solutions to this, I prefer the approach using the 'docker/entrypoint.sh' scripts that are in the 'client' and 'server' directories.


Be sure to change the environment variables (DATABASE_URL, API_URL) in docker-compose.yml according to your setup. Default should work if running on localhost.


### Warnings

Warning: If you run 'npm install' locally in the server or client folders, you'll need to delete 'node_modules' before running again with the docker setup. The binaries need to be install in the container's OS to work.


