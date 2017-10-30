# Docker Container for Logitech Media Server

This is a Docker image for running the Logitech Media Server package
(aka SqueezeboxServer).

Run Directly:

    docker run -d \
               --name SqueezeboxServer \
               -p 9000:9000 \
               -p 3483:3483 \
               -p 3483:3483/udp \
               -p 4070:4070 \
               -v /etc/localtime:/etc/localtime:ro \
               -v /share/CACHEDEV1_DATA/lms_state:/srv/squeezebox \
               -v /share/music:/srv/music \
               schwingsk/docker-image-logitech-media-server
