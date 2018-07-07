# Tutorial for Docker

Code and process from: https://docs.docker.com/get-started/part2/#apppy

Docker public repository: https://hub.docker.com/r/coelomate/docker-tutorial-one/

# Build command:

docker build -t friendlyhello .

# Run command:

docker run -p 4000:80 friendlyhello

or background mode

docker run -d -p 4000:80 friendlyhello

# Stop command:

First, list containers with:

docker container ls

Then, pick the one to stop with:

docker container stop [container id]

docker container stop ef41fda4bbe1

# Test it:

Visit localhost at: http://localhost:4000

or use:

curl http://localhost:4000

# Tag it:

docker tag friendlyhello coelomate/docker-tutorial-one:part2

# Publish it:

docker push coelomate/docker-tutorial-one:part2

# Pull it and run it locally:

docker pull coelomate/docker-tutorial-one

docker run -p 4000:80 coelomate/docker-tutorial-one:part2

# Later / TODO: Part 3:

https://docs.docker.com/get-started/part3/
