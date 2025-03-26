# YACE (Yet-Another-Cloudwatch-Exporter) docker compose

## Usage

```bash
# run as detach mode
docker compose up -d
```

## yace config

see [github.com/prometheus-community/yet-another-cloudwatch-exporter/docs/configuration.md](https://github.com/prometheus-community/yet-another-cloudwatch-exporter/blob/master/docs/configuration.md)

> copied configuration text from yace repo.

Below are the top level fields of the YAML configuration file:

```yaml
# Configuration file version. Must be set to "v1alpha1" currently.
apiVersion: v1alpha1

# STS regional endpoint (optional)
[ sts-region: <string>]

# Note that at least one of the following blocks must be defined.

# Configurations for jobs of type "auto-discovery"
discovery: <discovery_jobs_list_config>

# Configurations for jobs of type "static"
static:
  [ - <static_job_config> ... ]

# Configurations for jobs of type "custom namespace"
customNamespace:
  [ - <custom_namespace_job_config> ... ]
```

Note that while the `discovery`, `static` and `customNamespace` blocks are all optionals, at least one of them must be defined.

---

## References

- [prometheus-community/yet-another-cloudwatch-exporter/docker-compose](https://github.com/prometheus-community/yet-another-cloudwatch-exporter/tree/master/docker-compose)
- [prometheus-community/yet-another-cloudwatch-exporter/examples/rds.yml](https://github.com/prometheus-community/yet-another-cloudwatch-exporter/blob/master/examples/rds.yml)
