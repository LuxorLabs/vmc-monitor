# vmc-monitor
Scrape basic metrics from a VM and containers running in it for monitoring

## Update the following if you are using VictoriaMetrics

### `docker-compose.yaml
```yaml
      - '--remoteWrite.url="<DEFINE_ME>"'
      - '--remoteWrite.basicAuth.password="<DEFINE_ME>"'
      - '--remoteWrite.basicAuth.username="<DEFINE_ME>"'
      - '--remoteWrite.headers=X-Scope-OrgID:<DEFINE_ME' # use for Grafana Mimir
```

Additionally, pay attention to your volume mount to ensure disk space is available.

### `vmagent.yaml
```yaml
  external_labels: # add labels e.g.
    machine_origin: my-machine
    foo: bar
```
