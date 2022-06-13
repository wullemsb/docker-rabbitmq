# RabbitMQ with streaming
This repository contains the [RabbitMQ](https://hub.docker.com/_/rabbitmq) **management-alpine** image with [delayed message exchange](https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/) plugin and [streaming](https://www.rabbitmq.com/stream.html) plugin enabled.

# Docker

Build the adapted container image through:

~~~~
docker build -t rabbitmq-streaming
~~~~

If you want to run this container locally(through localhost), use the following command:

~~~~
docker run -p 15672:15672 -p 5552:5552 -e RABBITMQ_SERVER_ADDITIONAL_ERL_ARGS="-rabbitmq_stream advertised_host localhost" rabbitmq-streaming
~~~~

More information why this is necessary can be found [here](https://github.com/rabbitmq/rabbitmq-stream-dotnet-client/issues/114).

## Documentation

The [documentation](https://hub.docker.com/_/rabbitmq/) is the same as the default management-alpine image.
