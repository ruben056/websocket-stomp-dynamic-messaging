# Dynamic topics using Websockets and Stomp (and Spring Boot)

## What

After the websocket session has been established, stomp takes care of the routing of all the messages.
Any client can listen to any topic, and send to any topics he wants.

You can also use wildcards in the topics for instance:
* listening to : `/topic/*/*`  --> receives messages send to `/topic/a/b` , `/topic/qsdfqsdf/ddd` , ... but not `/topic/a/b/c` , ...
* listening to : `/topic/**/*` --> receives message sent to all destinations starting with : `/topic/`

Can by really handy for testing.

## Running

`mvn spring-boot:run`

Then connect to `http://localhost:8080`
