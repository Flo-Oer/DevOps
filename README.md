# question

## 1-1 For which reason is it better to run the container with a flag -e to give the environment variables rather than put them directly in the Dockerfile?
 Passing environment variables with the -e flag when running a container is more secure, flexible, and reusable than hardcoding them in the Dockerfile. It allows for better security of sensitive data, easier updates, and simplifies managing configurations across different environments.

## 1-2 Why do we need a volume to be attached to our postgres container?
Volumes allow data to survive container restarts, upgrades, or recreations, ensuring data durability and backup capability.
so  we need a volume because when we stop the data we ensure that the data won't get lost

## 1-3 Document your database container essentials: commands and Dockerfile.
Run the Postgres container with environment variables and volume
docker run -d --name my-postgres-container --network app-network -e POSTGRES_USER=usr -e POSTGRES_PASSWORD=pwd -e POSTGRES_DB=db -v pgdata:/var/lib/postgresql/data postgres

View logs to see if there is any problem
docker logs my-postgres-container


## 1-4 Why do we need a multistage build? And explain each step of this dockerfile.
To separate the build environment (we used maven) from the final runtime environment, making the final image smaller and more secure. so we have two stages the build one and the runtime

## 1-5 Why do we need a reverse proxy?
We need it to Keeping your backend safe and hiding its address, sharing the work between several servers,
sending requests to the right service under one website, making pages load faster with caching and compression, giving users one easy address to access everything.

## 1-6 Why is docker-compose so important?
Docker Compose allows you to define and manage multiple related containers easily using a single YAML file.

## 1-7 Document docker-compose most important commands.
docker-compose up -d — start in detached mode.
docker-compose down — stop and remove containers, networks.
docker-compose build — build or rebuild images.
docker-compose logs — view logs from services.
docker-compose ps — list running containers.

## 1-8 Document your docker-compose file.

## 1-9 Document your publication commands and published images in dockerhub.

## 1-10 Why do we put our images into an online repo?

## 2-1 What are testcontainers?

## 2-2 For what purpose do we need to use secured variables ?

## 2-3 Why did we put needs: build-and-test-backend on this job? Maybe try without this and you will see!

## 2-4 For what purpose do we need to push docker images?
