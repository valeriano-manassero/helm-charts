# clearml

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.2](https://img.shields.io/badge/AppVersion-1.0.2-informational?style=flat-square)

MLOps platform

**Homepage:** <https://allegro.ai>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| valeriano-manassero | valeriano.manassero@gmail.com |  |

## Source Code

* <https://github.com/valeriano-manassero/helm-charts>
* <https://github.com/allegroai/clearml>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | mongodb | ~10.3.2 |
| https://charts.bitnami.com/bitnami | redis | ~10.9.0 |
| https://helm.elastic.co | elasticsearch | ~7.10.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| agentGroups.agent-group0.affinity | object | `{}` |  |
| agentGroups.agent-group0.agentVersion | string | `""` |  |
| agentGroups.agent-group0.awsAccessKeyId | string | `nil` |  |
| agentGroups.agent-group0.awsDefaultRegion | string | `nil` |  |
| agentGroups.agent-group0.awsSecretAccessKey | string | `nil` |  |
| agentGroups.agent-group0.azureStorageAccount | string | `nil` |  |
| agentGroups.agent-group0.azureStorageKey | string | `nil` |  |
| agentGroups.agent-group0.clearmlAccessKey | string | `nil` |  |
| agentGroups.agent-group0.clearmlConfig | string | `"sdk {\n}"` |  |
| agentGroups.agent-group0.clearmlGitPassword | string | `nil` |  |
| agentGroups.agent-group0.clearmlGitUser | string | `nil` |  |
| agentGroups.agent-group0.clearmlSecretKey | string | `nil` |  |
| agentGroups.agent-group0.image.pullPolicy | string | `"IfNotPresent"` |  |
| agentGroups.agent-group0.image.repository | string | `"nvidia/cuda"` |  |
| agentGroups.agent-group0.image.tag | string | `"11.0-base-ubuntu18.04"` |  |
| agentGroups.agent-group0.name | string | `"agent-group0"` |  |
| agentGroups.agent-group0.nodeSelector | object | `{}` |  |
| agentGroups.agent-group0.nvidiaGpusPerAgent | int | `1` |  |
| agentGroups.agent-group0.podAnnotations | object | `{}` |  |
| agentGroups.agent-group0.queues | string | `"default"` |  |
| agentGroups.agent-group0.replicaCount | int | `0` |  |
| agentGroups.agent-group0.tolerations | list | `[]` |  |
| agentservices.affinity | object | `{}` |  |
| agentservices.agentVersion | string | `""` |  |
| agentservices.awsAccessKeyId | string | `nil` |  |
| agentservices.awsDefaultRegion | string | `nil` |  |
| agentservices.awsSecretAccessKey | string | `nil` |  |
| agentservices.azureStorageAccount | string | `nil` |  |
| agentservices.azureStorageKey | string | `nil` |  |
| agentservices.clearmlFilesHost | string | `nil` |  |
| agentservices.clearmlGitPassword | string | `nil` |  |
| agentservices.clearmlGitUser | string | `nil` |  |
| agentservices.clearmlHostIp | string | `nil` |  |
| agentservices.clearmlWebHost | string | `nil` |  |
| agentservices.clearmlWorkerId | string | `"clearml-services"` |  |
| agentservices.extraEnvs | list | `[]` |  |
| agentservices.googleCredentials | string | `nil` |  |
| agentservices.image.pullPolicy | string | `"IfNotPresent"` |  |
| agentservices.image.repository | string | `"allegroai/clearml-agent-services"` |  |
| agentservices.image.tag | string | `"latest"` |  |
| agentservices.nodeSelector | object | `{}` |  |
| agentservices.podAnnotations | object | `{}` |  |
| agentservices.replicaCount | int | `1` |  |
| agentservices.resources | object | `{}` |  |
| agentservices.storage.data.class | string | `"standard"` |  |
| agentservices.storage.data.size | string | `"50Gi"` |  |
| agentservices.tolerations | list | `[]` |  |
| apiserver.affinity | object | `{}` |  |
| apiserver.configDir | string | `"/opt/clearml/config"` |  |
| apiserver.extraEnvs | list | `[]` |  |
| apiserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| apiserver.image.repository | string | `"allegroai/clearml"` |  |
| apiserver.image.tag | string | `"1.0.2"` |  |
| apiserver.livenessDelay | int | `60` |  |
| apiserver.nodeSelector | object | `{}` |  |
| apiserver.podAnnotations | object | `{}` |  |
| apiserver.prepopulateArtifactsPath | string | `"/mnt/fileserver"` |  |
| apiserver.prepopulateEnabled | string | `"true"` |  |
| apiserver.prepopulateZipFiles | string | `"/opt/clearml/db-pre-populate"` |  |
| apiserver.readinessDelay | int | `60` |  |
| apiserver.replicaCount | int | `1` |  |
| apiserver.resources | object | `{}` |  |
| apiserver.service.port | int | `8008` |  |
| apiserver.service.type | string | `"NodePort"` |  |
| apiserver.storage.config.class | string | `"standard"` |  |
| apiserver.storage.config.size | string | `"1Gi"` |  |
| apiserver.storage.enableConfigVolume | bool | `false` |  |
| apiserver.tolerations | list | `[]` |  |
| clearml.defaultCompany | string | `"d1bd92a3b039400cbafc60a7a5b1e52b"` |  |
| elasticsearch.clusterHealthCheckParams | string | `"wait_for_status=yellow&timeout=1s"` |  |
| elasticsearch.clusterName | string | `"clearml-elastic"` |  |
| elasticsearch.enabled | bool | `true` |  |
| elasticsearch.esConfig."elasticsearch.yml" | string | `"xpack.security.enabled: false\n"` |  |
| elasticsearch.esJavaOpts | string | `"-Xmx2g -Xms2g"` |  |
| elasticsearch.extraEnvs[0].name | string | `"bootstrap.memory_lock"` |  |
| elasticsearch.extraEnvs[0].value | string | `"true"` |  |
| elasticsearch.extraEnvs[1].name | string | `"cluster.routing.allocation.node_initial_primaries_recoveries"` |  |
| elasticsearch.extraEnvs[1].value | string | `"500"` |  |
| elasticsearch.extraEnvs[2].name | string | `"cluster.routing.allocation.disk.watermark.low"` |  |
| elasticsearch.extraEnvs[2].value | string | `"500mb"` |  |
| elasticsearch.extraEnvs[3].name | string | `"cluster.routing.allocation.disk.watermark.high"` |  |
| elasticsearch.extraEnvs[3].value | string | `"500mb"` |  |
| elasticsearch.extraEnvs[4].name | string | `"cluster.routing.allocation.disk.watermark.flood_stage"` |  |
| elasticsearch.extraEnvs[4].value | string | `"500mb"` |  |
| elasticsearch.extraEnvs[5].name | string | `"http.compression_level"` |  |
| elasticsearch.extraEnvs[5].value | string | `"7"` |  |
| elasticsearch.extraEnvs[6].name | string | `"reindex.remote.whitelist"` |  |
| elasticsearch.extraEnvs[6].value | string | `"*.*"` |  |
| elasticsearch.extraEnvs[7].name | string | `"xpack.monitoring.enabled"` |  |
| elasticsearch.extraEnvs[7].value | string | `"false"` |  |
| elasticsearch.extraEnvs[8].name | string | `"xpack.security.enabled"` |  |
| elasticsearch.extraEnvs[8].value | string | `"false"` |  |
| elasticsearch.httpPort | int | `9200` |  |
| elasticsearch.image | string | `"docker.elastic.co/elasticsearch/elasticsearch"` |  |
| elasticsearch.imageTag | string | `"7.6.2"` |  |
| elasticsearch.minimumMasterNodes | int | `1` |  |
| elasticsearch.name | string | `"{{ .Release.Name }}-elastic-master"` |  |
| elasticsearch.persistence.enabled | bool | `true` |  |
| elasticsearch.replicas | int | `1` |  |
| elasticsearch.resources.limits.memory | string | `"4Gi"` |  |
| elasticsearch.resources.requests.memory | string | `"4Gi"` |  |
| elasticsearch.roles.data | string | `"true"` |  |
| elasticsearch.roles.ingest | string | `"true"` |  |
| elasticsearch.roles.master | string | `"true"` |  |
| elasticsearch.volumeClaimTemplate.accessModes[0] | string | `"ReadWriteOnce"` |  |
| elasticsearch.volumeClaimTemplate.resources.requests.storage | string | `"50Gi"` |  |
| fileserver.affinity | object | `{}` |  |
| fileserver.extraEnvs | list | `[]` |  |
| fileserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| fileserver.image.repository | string | `"allegroai/clearml"` |  |
| fileserver.image.tag | string | `"1.0.2"` |  |
| fileserver.nodeSelector | object | `{}` |  |
| fileserver.podAnnotations | object | `{}` |  |
| fileserver.replicaCount | int | `1` |  |
| fileserver.resources | object | `{}` |  |
| fileserver.service.port | int | `8081` |  |
| fileserver.service.type | string | `"NodePort"` |  |
| fileserver.storage.data.class | string | `"standard"` |  |
| fileserver.storage.data.size | string | `"50Gi"` |  |
| fileserver.tolerations | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.host | string | `""` |  |
| ingress.name | string | `"clearml-server-ingress"` |  |
| ingress.tls.secretName | string | `""` |  |
| mongodb.architecture | string | `"standalone"` |  |
| mongodb.auth.enabled | bool | `false` |  |
| mongodb.enabled | bool | `true` |  |
| mongodb.image.registry | string | `"docker.io"` |  |
| mongodb.image.repository | string | `"bitnami/mongodb"` |  |
| mongodb.image.tag | string | `"3.6.21-debian-9-r71"` |  |
| mongodb.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| mongodb.persistence.enabled | bool | `true` |  |
| mongodb.persistence.size | string | `"50Gi"` |  |
| mongodb.replicaCount | int | `1` |  |
| mongodb.service.name | string | `"{{ .Release.Name }}-mongodb"` |  |
| mongodb.service.port | int | `27017` |  |
| mongodb.service.portName | string | `"mongo-service"` |  |
| mongodb.service.type | string | `"ClusterIP"` |  |
| redis.cluster.enabled | bool | `false` |  |
| redis.databaseNumber | int | `0` |  |
| redis.enabled | bool | `true` |  |
| redis.image.registry | string | `"docker.io"` |  |
| redis.image.repository | string | `"bitnami/redis"` |  |
| redis.image.tag | string | `"5.0.10-debian-10-r88"` |  |
| redis.master.name | string | `"{{ .Release.Name }}-redis-master"` |  |
| redis.master.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| redis.master.persistence.enabled | bool | `true` |  |
| redis.master.persistence.size | string | `"5Gi"` |  |
| redis.master.port | int | `6379` |  |
| redis.usePassword | bool | `false` |  |
| webserver.affinity | object | `{}` |  |
| webserver.extraEnvs | list | `[]` |  |
| webserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| webserver.image.repository | string | `"allegroai/clearml"` |  |
| webserver.image.tag | string | `"1.0.2"` |  |
| webserver.nodeSelector | object | `{}` |  |
| webserver.podAnnotations | object | `{}` |  |
| webserver.replicaCount | int | `1` |  |
| webserver.resources | object | `{}` |  |
| webserver.service.port | int | `80` |  |
| webserver.service.type | string | `"NodePort"` |  |
| webserver.tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
