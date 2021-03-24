# <CHARTNAME>

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.1](https://img.shields.io/badge/AppVersion-1.0.1-informational?style=flat-square)

Helm v3 starter chart

**Homepage:** <https://github.com/waltlenu/charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| waltlenu | waltlenu@users.noreply.github.com |  |

## Source Code

* <https://github.com/waltlenu/charts>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.annotations | object | `{}` |  |
| autoscaling.create | bool | `false` |  |
| autoscaling.labels | object | `{}` |  |
| autoscaling.maxReplicas | int | `10` |  |
| autoscaling.metrics[0].resource.name | string | `"cpu"` |  |
| autoscaling.metrics[0].resource.target.averageUtilization | int | `50` |  |
| autoscaling.metrics[0].resource.target.type | string | `"Utilization"` |  |
| autoscaling.metrics[0].type | string | `"Resource"` |  |
| autoscaling.metrics[1].resource.name | string | `"memory"` |  |
| autoscaling.metrics[1].resource.target.averageUtilization | int | `50` |  |
| autoscaling.metrics[1].resource.target.type | string | `"Utilization"` |  |
| autoscaling.metrics[1].type | string | `"Resource"` |  |
| autoscaling.metrics[2].pods.metric.name | string | `"http_requests"` |  |
| autoscaling.metrics[2].pods.target.averageValue | string | `"500m"` |  |
| autoscaling.metrics[2].pods.target.type | string | `"AverageValue"` |  |
| autoscaling.metrics[2].type | string | `"Pods"` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.name | string | `nil` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| configMap.annotations | object | `{}` |  |
| configMap.create | bool | `false` |  |
| configMap.glob.enabled | bool | `false` |  |
| configMap.glob.pattern | string | `"confs/*"` |  |
| configMap.labels | object | `{}` |  |
| configMap.loadAsEnvVars | bool | `false` |  |
| configMap.mount.enabled | bool | `false` |  |
| configMap.mount.name | string | `"config"` |  |
| configMap.mount.path | string | `"/etc/config"` |  |
| configMap.name | string | `nil` |  |
| configMap.values | object | `{}` |  |
| containerPorts[0].containerPort | int | `8080` |  |
| containerPorts[0].name | string | `"http"` |  |
| containerPorts[0].protocol | string | `"TCP"` |  |
| dnsPolicy | string | `"ClusterFirst"` |  |
| extraArgs | object | `{}` |  |
| extraContainers | list | `[]` |  |
| extraEnvs | list | `[]` |  |
| extraInitContainers | list | `[]` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `nil` |  |
| hostNetwork | bool | `false` |  |
| image.command | string | `nil` |  |
| image.pullPolicy | string | `nil` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"waltlenu/caddy"` |  |
| image.tag | string | `"latest"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.certManager.clusterIssuerName | string | `nil` |  |
| ingress.certManager.create | bool | `false` |  |
| ingress.certManager.issuerName | string | `nil` |  |
| ingress.create | bool | `true` |  |
| ingress.externalDns | bool | `false` |  |
| ingress.extraHosts | string | `nil` |  |
| ingress.extraTls | string | `nil` |  |
| ingress.hostname | string | `"app.local"` |  |
| ingress.labels | object | `{}` |  |
| ingress.name | string | `nil` |  |
| ingress.path | string | `nil` |  |
| ingress.pathType | string | `nil` |  |
| ingress.tls | bool | `false` |  |
| kind | string | `"Deployment"` |  |
| lifecycle | object | `{}` |  |
| livenessProbe | object | `{}` |  |
| metrics.create | bool | `false` |  |
| metrics.prometheusRule.additionalLabels | object | `{}` |  |
| metrics.prometheusRule.enabled | bool | `false` |  |
| metrics.prometheusRule.namespace | string | `""` |  |
| metrics.prometheusRule.rules | list | `[]` |  |
| metrics.serviceMonitor.annotations | object | `{}` |  |
| metrics.serviceMonitor.create | bool | `true` |  |
| metrics.serviceMonitor.endpoints[0].interval | string | `"30s"` |  |
| metrics.serviceMonitor.endpoints[0].path | string | `"/metrics"` |  |
| metrics.serviceMonitor.endpoints[0].port | string | `"http"` |  |
| metrics.serviceMonitor.labels | object | `{}` |  |
| metrics.serviceMonitor.name | string | `nil` |  |
| minReadySeconds | int | `0` |  |
| nameOverride | string | `nil` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.create | bool | `false` |  |
| persistence.emptyDir | string | `nil` |  |
| persistence.existingClaim | string | `nil` |  |
| persistence.existingVolume | string | `nil` |  |
| persistence.labels | object | `{}` |  |
| persistence.name | string | `"data"` |  |
| persistence.path | string | `"/data"` |  |
| persistence.size | string | `"1Gi"` |  |
| persistence.storageClass | string | `nil` |  |
| podAnnotations | object | `{}` |  |
| podDisruptionBudget.annotations | object | `{}` |  |
| podDisruptionBudget.create | bool | `false` |  |
| podDisruptionBudget.labels | object | `{}` |  |
| podDisruptionBudget.maxUnavailable | string | `nil` |  |
| podDisruptionBudget.minAvailable | int | `1` |  |
| podDisruptionBudget.name | string | `nil` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.fsGroup | string | `nil` |  |
| podSecurityContext.runAsGroup | string | `nil` |  |
| podSecurityContext.runAsUser | string | `nil` |  |
| podSecurityPolicy.annotations | object | `{}` |  |
| podSecurityPolicy.create | bool | `true` |  |
| podSecurityPolicy.labels | object | `{}` |  |
| podSecurityPolicy.name | string | `nil` |  |
| priorityClassName | string | `""` |  |
| rbac.annotations | object | `{}` |  |
| rbac.clusterroleRules | string | `nil` |  |
| rbac.create | bool | `false` |  |
| rbac.labels | object | `{}` |  |
| rbac.name | string | `nil` |  |
| rbac.roleRules | string | `nil` |  |
| readinessProbe | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | string | `"250m"` |  |
| resources.limits.memory | string | `"256Mi"` |  |
| resources.requests.cpu | string | `"125m"` |  |
| resources.requests.memory | string | `"128Mi"` |  |
| revisionHistoryLimit | int | `10` |  |
| secret.annotations | object | `{}` |  |
| secret.create | bool | `false` |  |
| secret.labels | object | `{}` |  |
| secret.loadAsEnvVars | bool | `false` |  |
| secret.mount.enabled | bool | `false` |  |
| secret.mount.name | string | `"secret"` |  |
| secret.mount.path | string | `"/etc/secret"` |  |
| secret.name | string | `nil` |  |
| secret.type | string | `"Opaque"` |  |
| secret.values | object | `{}` |  |
| securityContext.allowPrivilegeEscalation | bool | `false` |  |
| securityContext.runAsGroup | int | `10000` |  |
| securityContext.runAsUser | int | `10000` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `nil` |  |
| service.create | bool | `true` |  |
| service.externalIPs | list | `[]` |  |
| service.externalTrafficPolicy | string | `""` |  |
| service.healthCheckNodePort | int | `0` |  |
| service.labels | object | `{}` |  |
| service.loadBalancerIP | string | `nil` |  |
| service.loadBalancerSourceRanges | list | `[]` |  |
| service.name | string | `nil` |  |
| service.ports[0].name | string | `"http"` |  |
| service.ports[0].nodePort | string | `nil` |  |
| service.ports[0].port | int | `8080` |  |
| service.ports[0].protocol | string | `"TCP"` |  |
| service.ports[0].targetPort | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.labels | object | `{}` |  |
| serviceAccount.name | string | `nil` |  |
| terminationGracePeriodSeconds | int | `60` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |
| updateStrategy | object | `{}` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
