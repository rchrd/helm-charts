# homeassistant

Home Assistant - Open source home automation that puts local control and privacy first.

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![AppVersion: 2020.12.0](https://img.shields.io/badge/AppVersion-2020.12.0-informational?style=flat-square)

## About the chart

This installation of Home Assistant uses a volume mount on the host to store persistent data.

## Example values file

```
dnsNames:
- hass.mydomain.com

hostPath: /data/homeassistant
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| dnsNames | list | `nil` | List of DNS names the ingress should respond to |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecret | string | `nil` |  |
| image.repository | string | `"docker.io/homeassistant/home-assistant"` |  |
| image.tag | string | `"2020.12.0"` |  |
| mountPath | string | `"/data"` | Path were the persistent data is stored on the host |
| replicaCount | int | `1` | Number of replicas to run |
| service.port | int | `8123` |  |
| service.type | string | `"ClusterIP"` |  |
| timezone | string | `"Europe/Amsterdam"` | Timezone |