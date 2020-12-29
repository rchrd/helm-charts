# homeassistant

Home Assistant - Open source home automation that puts local control and privacy first.

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![AppVersion: 2020.12.1](https://img.shields.io/badge/AppVersion-2020.12.1-informational?style=flat-square)

## About the chart

This installation of Home Assistant uses a volume mount on the host to store persistent data.

## Basic usage example

```
helm repo add rchrd https://rchrd.github.io/helm-charts/
helm repo update

helm template homeassistant rchrd/home-assistant --set dnsNames={hass.mydomain.com} --set mountPath=/data/homeassistant
```

## Configuration

The following table lists the configurable parameters of the chart and the default values.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| dnsNames | list | `nil` | List of DNS names the ingress should respond to |
| image.pullPolicy | string | `"IfNotPresent"` | Image pull policy |
| image.pullSecret | string | `nil` | Optional image pull secret |
| image.repository | string | `"docker.io/homeassistant/home-assistant"` | Image to use |
| image.tag | string | `"2020.12.1"` | Tag to use |
| mountPath | string | `"/tmp"` | Path were the persistent data is stored on the host (must exist before deployment) |
| replicaCount | int | `1` | Number of replicas to run |
| service.port | int | `8123` | Service port |
| service.type | string | `"ClusterIP"` | Service type |
| timezone | string | `"Europe/Amsterdam"` | Timezone |