# bitwarden

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.19.0](https://img.shields.io/badge/AppVersion-1.19.0-informational?style=flat-square)

Bitwarden RS password manager

**Homepage:** <https://github.com/waltlenu/charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| waltlenu | waltlenu@users.noreply.github.com |  |

## Source Code

* <https://github.com/dani-garcia/bitwarden_rs>

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
| extraEnvs[0].name | string | `"ROCKET_PORT"` |  |
| extraEnvs[0].value | string | `"8080"` |  |
| extraEnvs[1].name | string | `"SIGNUPS_ALLOWED"` |  |
| extraEnvs[1].value | string | `"false"` |  |
| extraEnvs[2].name | string | `"INVITATIONS_ALLOWED"` |  |
| extraEnvs[2].value | string | `"false"` |  |
| extraEnvs[3].name | string | `"ADMIN_TOKEN"` |  |
| extraEnvs[3].value | string | `"IDDQD"` |  |
| extraInitContainers | list | `[]` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `nil` |  |
| hostNetwork | bool | `false` |  |
| image.command | string | `nil` |  |
| image.pullPolicy | string | `nil` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"bitwardenrs/server"` |  |
| image.tag | string | `nil` |  |
| ingress.annotations | object | `{}` |  |
| ingress.certManager.clusterIssuerName | string | `"letsencrypt-production"` |  |
| ingress.certManager.create | bool | `false` |  |
| ingress.certManager.issuerName | string | `nil` |  |
| ingress.create | bool | `true` |  |
| ingress.externalDns | bool | `false` |  |
| ingress.extraHosts | string | `nil` |  |
| ingress.extraTls | string | `nil` |  |
| ingress.hostname | string | `"secrets.local"` |  |
| ingress.labels | object | `{}` |  |
| ingress.name | string | `nil` |  |
| ingress.path | string | `nil` |  |
| ingress.pathType | string | `nil` |  |
| ingress.tls | bool | `false` |  |
| kind | string | `"StatefulSet"` |  |
| lifecycle | object | `{}` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | int | `8080` |  |
| livenessProbe.httpGet.scheme | string | `"HTTP"` |  |
| livenessProbe.initialDelaySeconds | int | `5` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
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
| persistence.create | bool | `true` |  |
| persistence.emptyDir | string | `nil` |  |
| persistence.existingClaim | string | `nil` |  |
| persistence.existingVolume | string | `nil` |  |
| persistence.labels | object | `{}` |  |
| persistence.name | string | `"data"` |  |
| persistence.path | string | `"/data"` |  |
| persistence.size | string | `"256Mi"` |  |
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
| podSecurityContext.runAsGroup | int | `10000` |  |
| podSecurityContext.runAsUser | int | `10000` |  |
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
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | int | `8080` |  |
| readinessProbe.httpGet.scheme | string | `"HTTP"` |  |
| readinessProbe.initialDelaySeconds | int | `5` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
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
| securityContext.runAsGroup | string | `nil` |  |
| securityContext.runAsUser | string | `nil` |  |
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
