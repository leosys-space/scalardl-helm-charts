# envoy

envoy.
Current chart version is `1.0.2`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envoy.affinity | object | `{}` | the affinity/anti-affinity feature, greatly expands the types of constraints you can express |
| envoy.envoyConfiguration.adminAccessLogPath | string | `"/dev/stdout"` | admin log path |
| envoy.grafanaDashboard.enabled | bool | `false` |  |
| envoy.grafanaDashboard.namespace | string | `"monitoring"` |  |
| envoy.image.pullPolicy | string | `"IfNotPresent"` | Specify a imagePullPolicy |
| envoy.image.repository | string | `"ghcr.io/leosys-space/scalar-envoy"` | Docker image |
| envoy.image.version | string | `"1.0.11"` |  |
| envoy.imagePullSecrets | list | `[]` | Optionally specify an array of imagePullSecrets. Secrets must be manually created in the namespace. |
| envoy.nodeSelector | object | `{}` | nodeSelector is form of node selection constraint |
| envoy.podSecurityContext | object | `{}` | PodSecurityContext holds pod-level security attributes and common container settings |
| envoy.prometheusRule.enabled | bool | `false` | enable rules for prometheus |
| envoy.prometheusRule.namespace | string | `"monitoring"` | which namespace prometheus is located. by default monitoring |
| envoy.replicaCount | int | `3` | number of replicas to deploy |
| envoy.resources | object | `{}` | resources allowed to the pod |
| envoy.securityContext | object | `{}` | Setting security context at the pod applies those settings to all containers in the pod |
| envoy.service.annotations | object | `{}` | Service annotations, e.g: prometheus, etc. |
| envoy.service.ports.envoy-priv.port | int | `50052` | nvoy public port |
| envoy.service.ports.envoy-priv.protocol | string | `"TCP"` | envoy protocol |
| envoy.service.ports.envoy-priv.targetPort | int | `50052` | envoy k8s internal name |
| envoy.service.ports.envoy.port | int | `50051` | envoy public port |
| envoy.service.ports.envoy.protocol | string | `"TCP"` | envoy protocol |
| envoy.service.ports.envoy.targetPort | int | `50051` | envoy k8s internal name |
| envoy.service.type | string | `"ClusterIP"` | service types in kubernetes |
| envoy.serviceMonitor.enabled | bool | `false` | enable metrics collect with prometheus |
| envoy.serviceMonitor.interval | string | `"15s"` | custom interval to retrieve the metrics |
| envoy.serviceMonitor.namespace | string | `"monitoring"` | which namespace prometheus is located. by default monitoring |
| envoy.strategy.rollingUpdate | object | `{"maxSurge":"25%","maxUnavailable":"25%"}` | The number of pods that can be unavailable during the update process |
| envoy.strategy.type | string | `"RollingUpdate"` | New pods are added gradually, and old pods are terminated gradually, e.g: Recreate or RollingUpdate |
| envoy.tolerations | list | `[]` | Tolerations are applied to pods, and allow (but do not require) the pods to schedule onto nodes with matching taints. |
| fullnameOverride | string | `""` | String to fully override scalardl.fullname template |
| nameOverride | string | `""` | String to partially override scalardl.fullname template (will maintain the release name) |
