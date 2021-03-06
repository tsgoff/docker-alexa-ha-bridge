docker-alexa-ha-bridge
========

[![](https://images.microbadger.com/badges/image/bios/docker-yourls.svg)](http://microbadger.com/images/bios/docker-alexa-ha-bridge)

[![Docker build](https://dockeri.co/image/bios/docker-alexa-ha-bridge)](https://hub.docker.com/r/bios/docker-alexa-ha-bridge/)




https://github.com/bwssytems/ha-bridge  
https://github.com/armzilla/amazon-echo-ha-bridge  
https://registry.hub.docker.com/u/bios/docker-alexa-ha-bridge/  

**Docker image to start a ha-bridge container with alpine**

Use --net=host for functional UPnP discovery

Quickstart
----------

    docker run --name bridge -d --net=host bios/docker-alexa-ha-bridge

Options
-------
 - PORT="-Dserver.port=8080" 
 - KEY="-Dsecurity.key=Xfawer354WertSdf321234asd" 
 - IP="-Dserver.ip=192.168.1.1" 
 - CONFIG="-Dconfig.file=/home/me/data/myhabridge.config" 
 - GARDEN="-Dexec.garden=/bridge/" 
 

Example
-------
Mount backup file and define custom port

    docker run --name bridge -d --net=host \
    -v /bridge/data/:/bridge/data \
    -e PORT="-Dserver.port=8080" \
    -e KEY="-Dsecurity.key=Xfawer354WertSdf321234asd" \
    -e IP="-Dserver.ip=192.168.1.1" \
    -e GARDEN="-Dexec.garden=/bridge/" bios/docker-alexa-ha-bridge
