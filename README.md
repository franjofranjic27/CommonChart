# generic-chart

![Version: 0.2.1](https://img.shields.io/badge/Version-0.2.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

A generic Helm chart for deploying Services

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| deployment.enabled | bool | `true` |  |
| deployment.image.pullPolicy | string | `"IfNotPresent"` |  |
| deployment.image.repository | string | `"your-docker-repo"` |  |
| deployment.image.tag | string | `"latest"` |  |
| deployment.livenessProbe.failureThreshold | int | `3` |  |
| deployment.livenessProbe.httpGet.path | string | `"/api/actuator/health"` |  |
| deployment.livenessProbe.httpGet.port | int | `8080` |  |
| deployment.livenessProbe.initialDelaySeconds | int | `10` |  |
| deployment.livenessProbe.periodSeconds | int | `10` |  |
| deployment.livenessProbe.successThreshold | int | `1` |  |
| deployment.livenessProbe.timeoutSeconds | int | `5` |  |
| deployment.ports[0].containerPort | int | `8080` |  |
| deployment.ports[0].name | string | `"http"` |  |
| deployment.ports[0].protocol | string | `"TCP"` |  |
| deployment.readinessProbe.failureThreshold | int | `3` |  |
| deployment.readinessProbe.httpGet.path | string | `"/api/actuator/health"` |  |
| deployment.readinessProbe.httpGet.port | int | `8080` |  |
| deployment.readinessProbe.initialDelaySeconds | int | `10` |  |
| deployment.readinessProbe.periodSeconds | int | `10` |  |
| deployment.readinessProbe.successThreshold | int | `1` |  |
| deployment.readinessProbe.timeoutSeconds | int | `5` |  |
| deployment.replicaCount | int | `1` |  |
| deployment.resources.limits.cpu | string | `"500m"` |  |
| deployment.resources.limits.memory | string | `"512Mi"` |  |
| deployment.resources.requests.cpu | string | `"250m"` |  |
| deployment.resources.requests.memory | string | `"256Mi"` |  |
| deployment.startupProbe.failureThreshold | int | `12` |  |
| deployment.startupProbe.httpGet.path | string | `"/api/actuator/health"` |  |
| deployment.startupProbe.httpGet.port | int | `8080` |  |
| deployment.startupProbe.periodSeconds | int | `10` |  |
| deployment.strategy.maxSurge | string | `"25%"` |  |
| deployment.strategy.maxUnavailable | string | `"25%"` |  |
| deployment.strategy.type | string | `"RollingUpdate"` |  |
| global.appName | string | `"your-app-name"` |  |
| hpa.enabled | bool | `true` |  |
| hpa.maxReplicas | int | `3` |  |
| hpa.minReplicas | int | `1` |  |
| hpa.targetCPUUtilizationPercentage | int | `80` |  |
| ingress.enabled | bool | `false` |  |
| pdb.enabled | bool | `true` |  |
| pdb.minAvailable | int | `1` |  |
| service.enabled | bool | `true` |  |
| service.ports[0].name | string | `"http"` |  |
| service.ports[0].port | int | `8080` |  |
| service.ports[0].targetPort | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
