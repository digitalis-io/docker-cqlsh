# docker-cqlsh
## Standalone Docker Container for launching Cassandra CQLSH and connecting to Apache Cassandra

Place a cqlshrc file (https://cassandra.apache.org/doc/latest/tools/cqlsh.html#cqlshrc) in the cqlshrc directory (there is an example one there now) and pass this in to the cqlsh launcher script via the command line.

e.g 
```./cqlsh --cqlshrcfile /cqlshrc/cqlshrc.sample```

This will build the docker image locally if it doesnt already exist, mount the cqlshrc directory on the host into the container and then launch cqlsh by passing in the cqlshrc file command line argument.

The host directory is mounted in the container volume at ```/cqlshrc``` - if your using SSL and have any certs, pems etc.. you need to reference to connect then just put them in the cqlshrc host machine directory and they will be available to use in the container at that path. Make sure that the path to them in the cqlshrc files is pointing at the container path.
