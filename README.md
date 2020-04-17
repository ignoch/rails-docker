# Rails Bootstrap for Docker application

This is the basic setup to get a Rails application running on docker.
Other apps that install aside with rails are:
- Postgres
- Sidekiq
- Redis
- Nginx


Dockerfile.rails
----------------

This is used by create a new rails app to add or modify gems in case you 
needed to generate the real app

       docker build -t rails-toolbox \
              --build-arg USER_ID=$(id -u)  \
              --build-arg GROUP_ID=$(id -g) \
              -f Dockerfile.rails .

Dockerfile.nginx
----------------

Generates a reverse proxy for the app

Installation
------------
1. pull the repository
2. run `docker-compose up`
3. done