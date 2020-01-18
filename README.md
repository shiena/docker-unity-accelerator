# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

## Usage

Support only Asset Pipeline v2

```
docker-compose -f dokcer-compose.yml -f v2.yml -p v2 build
docker-compose -f dokcer-compose.yml -f v2.yml -p v2 up -d
```

Support both Asset Pipeline v2 and v1

```
docker-compose -f dokcer-compose.yml -f v1_2.yml -p v1_v2 build
docker-compose -f dokcer-compose.yml -f v1_2.yml -p v1_v2 up -d
```

