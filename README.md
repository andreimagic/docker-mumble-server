# Mumble Server

This is a Docker container for running Murmur server (Mumble).

# Usage

To build using this Dockerfile, run:

    docker build -t mumble-server .

To initialize the server configuration, run:

    docker run --name=mumble-server -d -p 64738:64738 -v /path/to/config/mumble-server:/data -t mumble-server:latest

The container will create a config file in `/path/to/config/mumble-server` and will launch the server on port 64738. If needed, edit the file, setting the server password etc. then restart.

    docker restart mumble-server

The log file will be created in `/path/to/config/mumble-server/mumble-server.log`, and the sqlite DB will be created in that directory as well.
