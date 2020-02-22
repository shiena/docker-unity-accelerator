# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

## Usage

Support only Asset Pipeline v2

```
# Build images
docker-compose -f dokcer-compose.yml -f v2.yml -p v2 build

# Run services
docker-compose -f dokcer-compose.yml -f v2.yml -p v2 up -d

# Show version
docker run --rm unity-accelerator:v2 /opt/Unity/accelerator/unity-accelerator --version
```

Support both Asset Pipeline v2 and v1

```
# Build images
docker-compose -f dokcer-compose.yml -f v1_2.yml -p v1_v2 build

# Run services
docker-compose -f dokcer-compose.yml -f v1_2.yml -p v1_v2 up -d

# Show version
docker run --rm unity-accelerator:v1_v2 /opt/Unity/accelerator/unity-accelerator --version
```

## Additional Services

- Grafana: http://localhost:3000/
    - default admin user is admin/admin
- Prometheus: http://localhost:9090/
