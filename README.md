# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

## Environment variables

`accelerator.env` example

```
COLLAB_REGISTRATION_TOKEN=ft0bJvbRD
DISABLE_USAGE_STATS=yes
```

see also
- https://hub.docker.com/r/unitytechnologies/accelerator
- https://docs.unity3d.com/Manual/UnityAccelerator.html#docker

## Usage

```
# Pull images
docker-compose pull

# Run services
docker-compose up -d
```

- Metrics reports: http://localhost:8080/metrics
- Health page: http://localhost:8080/api/health-agent

## Configuring dashboard account and password through command line
Go into accelerator container by executing `sh` inside it and run `unity-accelerator` in folder `/agent`.
```
sudo docker-compose exec accelerator sh
cd /agent
unity-accelerator dashboard password admin
```

## Additional Services

- Grafana: http://localhost:3000/
    - default admin user is admin/admin
- Prometheus: http://localhost:9090/
