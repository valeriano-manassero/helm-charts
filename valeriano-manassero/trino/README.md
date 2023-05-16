# trino

![Version: 4.0.1](https://img.shields.io/badge/Version-4.0.1-informational?style=flat-square) ![AppVersion: 380](https://img.shields.io/badge/AppVersion-380-informational?style=flat-square)

High performance, distributed SQL query engine for big data

**Homepage:** <https://trino.io>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| valeriano-manassero |  | <https://github.com/valeriano-manassero> |

## Source Code

* <https://github.com/valeriano-manassero/helm-charts>
* <https://github.com/trinodb/trino>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| accessControl | object | `{}` |  |
| auth | object | `{}` |  |
| catalogs | object | `{}` |  |
| clusterDomain | string | `"cluster.local"` |  |
| config.coordinator.affinity | object | `{}` |  |
| config.coordinator.env | list | `[]` |  |
| config.coordinator.extraConfig | string | `""` |  |
| config.coordinator.initContainers | list | `[]` |  |
| config.coordinator.jvm.gcMethod.g1.heapRegionSize | string | `"32M"` |  |
| config.coordinator.jvm.gcMethod.type | string | `"UseG1GC"` |  |
| config.coordinator.jvm.maxHeapSize | string | `"24G"` |  |
| config.coordinator.jvmExtraConfig | string | `""` |  |
| config.coordinator.nodeSelector | object | `{}` |  |
| config.coordinator.podAnnotations | object | `{}` |  |
| config.coordinator.replicas | int | `1` |  |
| config.coordinator.resources | object | `{}` |  |
| config.coordinator.tolerations | list | `[]` |  |
| config.general.authenticationType | string | `""` | Trino supports multiple authentication types: PASSWORD, CERTIFICATE, OAUTH2, JWT, KERBEROS For more info: https://trino.io/docs/current/security/authentication-types.html |
| config.general.catalogsMountType | string | `"secret"` |  |
| config.general.http.port | int | `8080` |  |
| config.general.httpsServer.enabled | bool | `false` |  |
| config.general.httpsServer.keystore.key | string | `""` |  |
| config.general.httpsServer.keystore.path | string | `"/usr/local/certs/clustercoord.pem"` |  |
| config.general.httpsServer.port | int | `8443` |  |
| config.general.internalCommunicationSharedSecret | string | `"some-secret"` |  |
| config.general.log.trino.level | string | `"INFO"` |  |
| config.general.node.dataDir | string | `"/data/trino"` |  |
| config.general.node.environment | string | `"production"` |  |
| config.general.node.pluginDir | string | `"/usr/lib/trino/plugin"` |  |
| config.general.path | string | `"/etc/trino"` |  |
| config.general.prestoCompatibleHeader | bool | `false` |  |
| config.general.processForwarded | bool | `false` |  |
| config.general.query.maxMemory | string | `"3GB"` |  |
| config.general.query.maxMemoryPerNode | string | `"1GB"` |  |
| config.general.query.maxTotalMemory | string | `"6GB"` |  |
| config.worker.affinity | object | `{}` |  |
| config.worker.autoscaler.enabled | bool | `false` |  |
| config.worker.autoscaler.maxReplicas | int | `5` |  |
| config.worker.autoscaler.stabilizationWindowSeconds | int | `300` |  |
| config.worker.autoscaler.targetCPUUtilizationPercentage | int | `50` |  |
| config.worker.env | list | `[]` |  |
| config.worker.extraConfig | string | `""` |  |
| config.worker.initContainers | list | `[]` |  |
| config.worker.jvm.gcMethod.g1.heapRegionSize | string | `"32M"` |  |
| config.worker.jvm.gcMethod.type | string | `"UseG1GC"` |  |
| config.worker.jvm.maxHeapSize | string | `"10G"` |  |
| config.worker.jvmExtraConfig | string | `""` |  |
| config.worker.nodeSelector | object | `{}` |  |
| config.worker.podAnnotations | object | `{}` |  |
| config.worker.replicas | int | `2` | Replica count when autoscaler is disabled. If autoscaler is enabled, it sets minimum number of replicas. |
| config.worker.resources | object | `{}` |  |
| config.worker.tolerations | list | `[]` |  |
| configMapMounts | list | `[]` |  |
| connectors | object | `{}` |  |
| eventListenerProperties | object | `{}` |  |
| faultTolerance.enabled | bool | `false` |  |
| groupProvider | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"trinodb/trino"` |  |
| image.securityContext.fsGroup | int | `1000` |  |
| image.securityContext.runAsGroup | int | `1000` |  |
| image.securityContext.runAsUser | int | `1000` |  |
| image.tag | int | `380` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.host | string | `""` |  |
| ingress.ingressClassName | string | `nil` |  |
| ingress.tls.secretName | string | `""` |  |
| initKeystore.image.pullPolicy | string | `"IfNotPresent"` |  |
| initKeystore.image.repository | string | `"bitnami/java"` |  |
| initKeystore.image.tag | int | `17` |  |
| jmxExporter.coordinator.enabled | bool | `false` |  |
| jmxExporter.downloadLink | string | `"https://repo1.maven.org/maven2/io/prometheus/jmx/jmx_prometheus_javaagent/0.17.2/jmx_prometheus_javaagent-0.17.2.jar"` |  |
| jmxExporter.image.pullPolicy | string | `"IfNotPresent"` |  |
| jmxExporter.image.repository | string | `"curlimages/curl"` |  |
| jmxExporter.image.tag | string | `"7.87.0"` |  |
| jmxExporter.jarfile | string | `"jmx_prometheus_javaagent-0.17.2.jar"` |  |
| jmxExporter.path | string | `"/prometheus"` |  |
| jmxExporter.port | int | `9000` |  |
| jmxExporter.serviceMonitor.additionalLabels | object | `{}` |  |
| jmxExporter.serviceMonitor.enabled | bool | `true` |  |
| jmxExporter.serviceMonitor.interval | string | `"1m"` |  |
| jmxExporter.serviceMonitor.path | string | `"/metrics"` |  |
| jmxExporter.serviceMonitor.port | string | `"jmx-exporter"` |  |
| jmxExporter.serviceMonitor.scrapeTimeout | string | `"10s"` |  |
| jmxExporter.worker.enabled | bool | `false` |  |
| resourceGroups | object | `{}` |  |
| schemas | object | `{}` |  |
| secretMounts | list | `[]` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tls.autoGenerated | bool | `false` |  |
| tls.existingKeystoreSecret | string | `""` |  |
| tls.internodeEncryption | bool | `false` |  |
| tls.keystorePasswordSecret | string | `""` |  |
| tls.resources | object | `{}` |  |
| tls.tlsEncryptionSecretName | string | `""` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
