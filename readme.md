# Spark Cluster on Docker

This repository provides an easy way to deploy an Apache Spark cluster locally using Docker and Docker Compose.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Make](https://www.gnu.org/software/make/)

## Getting Started

Clone the repository:

```bash
git clone https://github.com/yourusername/spark_cluster.git
cd spark_cluster
```

## Spawning the Spark Cluster

You can start the Spark cluster using Docker Compose. By default, the setup includes one Spark master and multiple Spark workers.

To start the cluster with 3 workers, run:

```bash
docker-compose up --scale spark-worker=3
```

This command will launch one Spark master and three Spark worker containers.

Alternatively, if you prefer using `make`, simply run:

```bash
make run
```

This will execute the necessary Docker Compose command to start the cluster.

## Accessing Spark UI

Once the cluster is running, you can access the Spark Web UI at [http://localhost:9090](http://localhost:9090).

## Stopping the Cluster

To stop and remove the containers, run:

```bash
docker-compose down
```

Or, using `make`:

```bash
make stop
```

## Customizing the Cluster

You can adjust the number of workers by changing the `--scale spark-worker=<number>` parameter or by modifying the `docker-compose.yml` file.

## License

This project is licensed under the MIT License.
