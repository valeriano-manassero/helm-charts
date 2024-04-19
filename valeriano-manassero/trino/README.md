# trino

![Version: 9.2.0](https://img.shields.io/badge/Version-9.2.0-informational?style=flat-square) ![AppVersion: 433](https://img.shields.io/badge/AppVersion-433-informational?style=flat-square)

High performance, distributed SQL query engine for big data

**Homepage:** <https://trino.io>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| valeriano-manassero |  | <https://github.com/valeriano-manassero> |

## Source Code

* <https://github.com/valeriano-manassero/helm-charts>
* <https://github.com/trinodb/trino>

## Requirements

Kubernetes: `>= 1.24.0-0 < 1.29.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| accessControl | object | `{}` |  |
| auth | object | `{}` |  |
| catalogs | object | `{}` |  |
| clusterDomain | string | `"cluster.local"` |  |
| config.coordinator.affinity | object | `{}` |  |
| config.coordinator.env | list | `[]` |  |
| config.coordinator.envFrom | list | `[]` |  |
| config.coordinator.extraConfig | string | `""` |  |
| config.coordinator.initContainers | list | `[]` |  |
| config.coordinator.jvm.gcMethod.g1.heapRegionSize | string | `"32M"` |  |
| config.coordinator.jvm.gcMethod.type | string | `"UseG1GC"` |  |
| config.coordinator.jvm.maxRAMPercentage | float | `80` |  |
| config.coordinator.jvmExtraConfig | string | `""` |  |
| config.coordinator.nodeSelector | object | `{}` |  |
| config.coordinator.podAnnotations | object | `{}` |  |
| config.coordinator.podLabels | object | `{}` |  |
| config.coordinator.query.maxMemoryPerNode | string | `"1GB"` |  |
| config.coordinator.replicas | int | `1` |  |
| config.coordinator.resources | object | `{}` |  |
| config.coordinator.tolerations | list | `[]` |  |
| config.general.authenticationType | string | `""` | Trino supports multiple authentication types: PASSWORD, CERTIFICATE, OAUTH2, JWT, KERBEROS For more info: https://trino.io/docs/current/security/authentication-types.html |
| config.general.catalogsMountType | string | `"secret"` |  |
| config.general.env | list | `[]` |  |
| config.general.envFrom | list | `[]` |  |
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
| config.general.query.maxTotalMemory | string | `"6GB"` |  |
| config.worker.affinity | object | `{}` |  |
| config.worker.autoscaler.enabled | bool | `false` |  |
| config.worker.autoscaler.maxReplicas | int | `5` |  |
| config.worker.autoscaler.stabilizationWindowSeconds | int | `300` |  |
| config.worker.autoscaler.targetCPUUtilizationPercentage | int | `50` |  |
| config.worker.env | list | `[]` |  |
| config.worker.envFrom | list | `[]` |  |
| config.worker.extraConfig | string | `""` |  |
| config.worker.extraVolumeMounts | object | `{}` |  |
| config.worker.extraVolumes | object | `{}` |  |
| config.worker.initContainers | list | `[]` |  |
| config.worker.jvm.gcMethod.g1.heapRegionSize | string | `"32M"` |  |
| config.worker.jvm.gcMethod.type | string | `"UseG1GC"` |  |
| config.worker.jvm.maxRAMPercentage | float | `80` |  |
| config.worker.jvmExtraConfig | string | `""` |  |
| config.worker.lifecycle | object | `{}` |  |
| config.worker.nodeSelector | object | `{}` |  |
| config.worker.podAnnotations | object | `{}` |  |
| config.worker.podLabels | object | `{}` |  |
| config.worker.query.maxMemoryPerNode | string | `"1GB"` |  |
| config.worker.replicas | int | `2` | Replica count when autoscaler is disabled. If autoscaler is enabled, it sets minimum number of replicas. |
| config.worker.resources | object | `{}` |  |
| config.worker.tolerations | list | `[]` |  |
| configMapMounts | list | `[]` |  |
| connectors | object | `{}` |  |
| containerSecurityContext | object | `{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]}}` | SecurityContext configuration for containers |
| eventListenerProperties | object | `{}` |  |
| faultTolerance.configAsSecret | bool | `true` |  |
| faultTolerance.enabled | bool | `false` |  |
| fullnameOverride | string | `"trino"` |  |
| groupProvider | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"trinodb/trino"` |  |
| image.tag | int | `433` |  |
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
| passwordAuthenticatorProperties | object | `{}` | Password authenticator configuration, an item per conf line. Requiere `config.general.authenticationType` set to `PASSWORD`. For file : you don't need to use this propertie if you set `config.general.authenticationType` to `PASSWORD` and use `config.auth` to fill `auth/password.db`. For LDAP : https://trino.io/docs/current/security/ldap.html. For SalesForce : https://trino.io/docs/current/security/salesforce.html |
| podSecurityContext | object | `{"fsGroup":1000,"runAsGroup":1000,"runAsNonRoot":true,"runAsUser":1000,"seccompProfile":{"type":"RuntimeDefault"}}` | SecurityContext configuration for pods |
| resourceGroups | object | `{}` |  |
| schemas | object | `{}` |  |
| secretMounts | list | `[]` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| serviceAnnotations | object | `{}` |  |
| tls.autoGenerated | bool | `false` |  |
| tls.existingKeystoreSecret | string | `""` |  |
| tls.internodeEncryption | bool | `false` |  |
| tls.keystorePasswordSecret | string | `""` |  |
| tls.resources | object | `{}` |  |
| tls.tlsEncryptionSecretName | string | `""` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.3](https://github.com/norwoodj/helm-docs/releases/v1.11.3)
