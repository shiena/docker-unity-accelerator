# docker-unity-accelerator
Docker images for Unity Accelerator with Prometheus and Grafana

## Environment variables

`accelerator.env` example

```
COLLAB_REGISTRATION_TOKEN=ft0bJvbRD
DISABLE_USAGE_STATS=yes
```

| Variable | Usage |
|---|---|
| COLLAB_REGISTRATION_TOKEN	| Accelerate [Unity Collaborate](https://unity3d.com/unity/features/collaborate) |
| DISABLE_USAGE_STATS | Set to true to disable usage stats – leaving usage stats enabled can help improve the Accelerator’s features and performance by giving Unity valuable feedback. |
| USER | The user name for the local, built-in dashboard. |
| PASSWORD | The password for the local, built-in dashboard. |
| CERT_HOSTNAME | The hostname to use for TLS support. This is used for redirects, etc. and goes along with CERT_PEM and KEY_PEM below. |
| CERT_PEM | The path to a cert.pem to use for TLS support. If you set CERT_HOSTNAME but do not set CERT_PEM, <persist_dir>/cert.pem will be assumed. |
| KEY_PEM | The path to a key.pem to use for TLS support. If you set CERT_HOSTNAME but do not set KEY_PEM, <persist_dir>/key.pem will be assumed. |


| variable | usage |
|----|----|
| UNITY_ACCELERATOR_PERSIST	| Container default is /agent. This is the directory where unity-accelerator.cfg resides as well as other persisted data (cachedir possibly being different). |
| UNITY_ACCELERATOR_LOG_STDOUT | Container default is true. This, if true, will output logs to stdout only; false if you want actual log files written within the persist directory. |

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
