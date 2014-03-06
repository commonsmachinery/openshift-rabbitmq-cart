openshift-rabbitmq-cart
=======================

Openshift cartridge providing the RabbitMQ message broker.  It does
not yet support clustered setups, but ought to work in a scaled
application.


Installation
------------

This cartridge depends on Erlang being installed in the system.  The
reason is that the runtime environment is a bit too big to be possible
to build or install as a cartridge without timeouts.

Ask your Openshift administrator to run this:

    yum install erlang

On RHEL-based systems the EPEL repository must first be added:
http://fedoraproject.org/wiki/EPEL/FAQ#howtouse


Add the cartridge from github:

    rhc cartridge add https://raw.github.com/commonsmachinery/openshift-rabbitmq-cart/master/metadata/manifest.yml -a MY_APP


Environment variables
---------------------

These are relevant to applications and other gears:

* `OPENSHIFT_RABBITMQ_URI`: Full `amqp:` URI, which is probably the
  only of these variables that you need to use.
* `OPENSHIFT_RABBITMQ_BROKER_HOST`: Hostname or IP of the broker
* `OPENSHIFT_RABBITMQ_BROKER_PORT`: Port the broker is listening on
* `OPENSHIFT_RABBITMQ_USERNAME`: Admin account username
* `OPENSHIFT_RABBITMQ_PASSWORD`: Admin account password
