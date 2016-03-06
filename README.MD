# Dynamic topics using Websockets and Stomp (and Spring Boot)

## What

After the websocket session has been established, stomp takes care of the routing of all the messages.
Any client can listen to any topic, and send to any topics he wants.

You can also use wildcards in the topics for instance:
listening to : `/topic/*/*`  --> will receive message send to `/topic/a/b` , `/topic/qsdfqsdf/ddd` , ... but not `/topic/a/b/c` , ...
listening to : `/topic/**/*` --> will receive message sent to all every destination startingn with : `/topic/`

Can by really handy for testing.

## Running

`mvn spring-boot:run`

Then connect to `http://localhost:8080`
