# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

## Environment variables

`accelerator.env` example

```
COLLAB_REGISTRATION_TOKEN=ft0bJvbRD
DISABLE_USAGE_STATS=yes
```

see also https://hub.docker.com/r/unitytechnologies/accelerator

## Usage

```
# Pull images
docker-compose pull

# Run services
docker-compose up -d
```

- Metrics reports: http://localhost:8080/metrics
- Health page: http://localhost:8080/api/health-agent

## Additional Services

- Grafana: http://localhost:3000/
    - default admin user is admin/admin
- Prometheus: http://localhost:9090/
