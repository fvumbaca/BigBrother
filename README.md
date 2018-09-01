# Local Metrics

A local metrics setup using Prometheus, Grafana, and Docker-Compose.

## Usage
In the project root, just run:
```bash
docker-compose up
```

Modify `prometheus.yml` to point to your local server(s).
> Note that when pointing from Prometheus to a local server, replace `localhost` with
> `host.docker.internal`.

This will start a Prometheus server on `localhost:9090`
and a Grafana server on `localhost:3030` with username and password of `admin` / `admin`. On fresh clones 
you will need to configure Grafana from scratch, but data
will be persisted between runs.


To stop:
```bash
docker-compose down
```
> NOTE: Grafana data is saved between runs,
> but Prometheus data is lost.

## Grafana Plugins

If you want to install Grafana plugins, install them to the `grafana-plugins` directory by passing
the `--pluginDir` flag to the Grafana CLI.
