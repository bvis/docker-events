# Docker Events
It exposes in STDOUT the `/events` endpoint of the docker API.

## Usage
For obtaining access to the docker API you need to mount the docker socket into the container.

    docker run --rm --volume /var/run/docker.sock:/var/run/docker.sock:ro basi/docker-events

It can be used to save the docker events in an ELK platform using the same config than the used for any other
container log.
