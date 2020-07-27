# docker-cqlsh
Docker Container for Cassandra CQLSH

Put a cqlshrc file in the cqlshrc directory and pass this in to the cqlsh script via the command line.

e.g ./cqlsh --cqlshrcfile /cqlshrc/cqlshrc.sample

This will build the docker image locally if it doesnt exist, mount the cqlshrc directory on the host into the container and then launch cqlsh by passing in the cqlshrc file command line argument.

The container volume is /cqlshrc - if your using SSL and have any certs, pems etc.. you need to reference to connect then just put them in the cqlshrc host machine directory and they will be available to use in the container.
