# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

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
