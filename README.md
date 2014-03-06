openshift-rabbitmq-cart
=======================

Openshift cartridge providing the RabbitMQ message broker.

*NOTE: This version does not yet support scaled apps!*


Installation
------------

The cartridge setup have to fetch the Erlang engine and Rabbit MQ
source code archives.  It will save them in /tmp and reuse them if
present when it has to re-setup, so you can speed up the cartridge add
operation by downloading them manually.  ssh onto the gear and run:

    wget https://packages.erlang-solutions.com/erlang/esl-erlang-src/otp_src_R16B03-1.tar.gz
    wget https://www.rabbitmq.com/releases/rabbitmq-server/v3.2.4/rabbitmq-server-generic-unix-3.2.4.tar.gz

Then add the cartridge as normal.
