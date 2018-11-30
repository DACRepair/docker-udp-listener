Docker image that listens on a specified UDP port, outputs to container log.

### Start it

By default, you can run it like this

    docker run -p 0.0.0.0:5005:5005 -p 0.0.0.0:5005:5005/udp --name udp-listener dacrepair/udp-listener

You can make it listen on another port

    docker run -p 0.0.0.0:4444:4444 -p 0.0.0.0:4444:4444/udp -e UDPPORT=4444 --name udp-listener dacrepair/udp-listener

#### Test it

In another terminal:

    nc -u localhost 5005

And start sending data.  You should see your text reflected in the `docker run` terminal
