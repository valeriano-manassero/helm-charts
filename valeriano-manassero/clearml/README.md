# clearml

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.17.4](https://img.shields.io/badge/AppVersion-1.17.4-informational?style=flat-square)

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
| agentGroups[0].affinity | object | `{}` |  |
| agentGroups[0].agentVersion | string | `""` |  |
| agentGroups[0].awsAccessKeyId | string | `nil` |  |
| agentGroups[0].awsDefaultRegion | string | `nil` |  |
| agentGroups[0].awsSecretAccessKey | string | `nil` |  |
| agentGroups[0].azureStorageAccount | string | `nil` |  |
| agentGroups[0].azureStorageKey | string | `nil` |  |
| agentGroups[0].clearmlAccessKey | string | `nil` |  |
| agentGroups[0].clearmlApiHost | string | `"http://apiserver-service:8008"` |  |
| agentGroups[0].clearmlConfig | string | `"sdk {\n}"` |  |
| agentGroups[0].clearmlFilesHost | string | `"http://fileserver-service:8081"` |  |
| agentGroups[0].clearmlGitPassword | string | `nil` |  |
| agentGroups[0].clearmlGitUser | string | `nil` |  |
| agentGroups[0].clearmlSecretKey | string | `nil` |  |
| agentGroups[0].clearmlWebHost | string | `"http://webserver-service"` |  |
| agentGroups[0].image.pullPolicy | string | `"IfNotPresent"` |  |
| agentGroups[0].image.repository | string | `"nvidia/cuda"` |  |
| agentGroups[0].image.tag | string | `"latest"` |  |
| agentGroups[0].name | string | `"agent-group0"` |  |
| agentGroups[0].nodeSelector | object | `{}` |  |
| agentGroups[0].nvidiaGpusPerAgent | int | `1` |  |
| agentGroups[0].podAnnotations | object | `{}` |  |
| agentGroups[0].queues | string | `"default"` |  |
| agentGroups[0].replicaCount | int | `0` |  |
| agentGroups[0].resources | object | `{}` |  |
| agentGroups[0].storage.data.class | string | `"standard"` |  |
| agentGroups[0].storage.data.size | string | `"50Gi"` |  |
| agentGroups[0].tolerations | list | `[]` |  |
| agentservices.affinity | object | `{}` |  |
| agentservices.agentVersion | string | `""` |  |
| agentservices.awsAccessKeyId | string | `nil` |  |
| agentservices.awsDefaultRegion | string | `nil` |  |
| agentservices.awsSecretAccessKey | string | `nil` |  |
| agentservices.azureStorageAccount | string | `nil` |  |
| agentservices.azureStorageKey | string | `nil` |  |
| agentservices.clearmlAccessKey | string | `nil` |  |
| agentservices.clearmlApiHost | string | `"http://apiserver-service:8008"` |  |
| agentservices.clearmlFilesHost | string | `nil` |  |
| agentservices.clearmlGitPassword | string | `nil` |  |
| agentservices.clearmlGitUser | string | `nil` |  |
| agentservices.clearmlHostIp | string | `nil` |  |
| agentservices.clearmlSecretKey | string | `nil` |  |
| agentservices.clearmlWebHost | string | `nil` |  |
| agentservices.clearmlWorkerId | string | `"clearml-services"` |  |
| agentservices.defaultBaseDocker | string | `"ubuntu:18.04"` |  |
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
| apiserver.deploymentType | string | `"Helm"` |  |
| apiserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| apiserver.image.repository | string | `"allegroai/clearml-server"` |  |
| apiserver.image.tag | string | `"latest"` |  |
| apiserver.nodeSelector | object | `{}` |  |
| apiserver.podAnnotations | object | `{}` |  |
| apiserver.prepopulateArtifactsPath | string | `"/mnt/fileserver"` |  |
| apiserver.prepopulateEnabled | string | `"true"` |  |
| apiserver.prepopulateZipFiles | string | `"/opt/clearml/db-pre-populate"` |  |
| apiserver.replicaCount | int | `1` |  |
| apiserver.resources | object | `{}` |  |
| apiserver.service.port | int | `8008` |  |
| apiserver.service.type | string | `"ClusterIP"` |  |
| apiserver.storage.config.class | string | `"standard"` |  |
| apiserver.storage.config.size | string | `"1Gi"` |  |
| apiserver.storage.logs.class | string | `"standard"` |  |
| apiserver.storage.logs.size | string | `"10Gi"` |  |
| apiserver.tolerations | list | `[]` |  |
| elasticsearch.enabled | bool | `true` |  |
| elasticsearch.esConfig."elasticsearch.yml" | string | `"xpack.security.enabled: false\n"` |  |
| elasticsearch.esJavaOpts | string | `"-Xmx2g -Xms2g"` |  |
| elasticsearch.httpPort | int | `9200` |  |
| elasticsearch.minimumMasterNodes | int | `1` |  |
| elasticsearch.persistence.enabled | bool | `true` |  |
| elasticsearch.replicas | int | `1` |  |
| elasticsearch.resources.limits.memory | string | `"4Gi"` |  |
| elasticsearch.resources.requests.memory | string | `"4Gi"` |  |
| elasticsearch.roles.data | string | `"true"` |  |
| elasticsearch.roles.ingest | string | `"true"` |  |
| elasticsearch.roles.master | string | `"true"` |  |
| elasticsearch.roles.remote_cluster_client | string | `"true"` |  |
| elasticsearch.volumeClaimTemplate.accessModes[0] | string | `"ReadWriteOnce"` |  |
| elasticsearch.volumeClaimTemplate.resources.requests.storage | string | `"50Gi"` |  |
| fileserver.affinity | object | `{}` |  |
| fileserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| fileserver.image.repository | string | `"allegroai/clearml-server"` |  |
| fileserver.image.tag | string | `"latest"` |  |
| fileserver.nodeSelector | object | `{}` |  |
| fileserver.podAnnotations | object | `{}` |  |
| fileserver.replicaCount | int | `1` |  |
| fileserver.resources | object | `{}` |  |
| fileserver.service.port | int | `8081` |  |
| fileserver.service.type | string | `"ClusterIP"` |  |
| fileserver.storage.data.class | string | `"standard"` |  |
| fileserver.storage.data.size | string | `"50Gi"` |  |
| fileserver.storage.logs.class | string | `"standard"` |  |
| fileserver.storage.logs.size | string | `"5Gi"` |  |
| fileserver.tolerations | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.host | string | `""` |  |
| ingress.name | string | `"clearml-server-ingress"` |  |
| ingress.tls.secretName | string | `""` |  |
| mongodb.architecture | string | `"standalone"` |  |
| mongodb.auth.enabled | bool | `false` |  |
| mongodb.enabled | bool | `true` |  |
| mongodb.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| mongodb.persistence.enabled | bool | `true` |  |
| mongodb.persistence.size | string | `"50Gi"` |  |
| mongodb.replicaCount | int | `1` |  |
| mongodb.service.port | int | `27017` |  |
| mongodb.service.portName | string | `"mongo-service"` |  |
| mongodb.service.type | string | `"ClusterIP"` |  |
| redis.cluster.enabled | bool | `false` |  |
| redis.databaseNumber | int | `0` |  |
| redis.enabled | bool | `true` |  |
| redis.master.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| redis.master.persistence.enabled | bool | `true` |  |
| redis.master.persistence.size | string | `"5Gi"` |  |
| redis.master.port | int | `6379` |  |
| redis.usePassword | bool | `false` |  |
| webserver.affinity | object | `{}` |  |
| webserver.image.pullPolicy | string | `"IfNotPresent"` |  |
| webserver.image.repository | string | `"allegroai/clearml-server"` |  |
| webserver.image.tag | string | `"latest"` |  |
| webserver.nodeSelector | object | `{}` |  |
| webserver.podAnnotations | object | `{}` |  |
| webserver.replicaCount | int | `1` |  |
| webserver.resources | object | `{}` |  |
| webserver.service.port | int | `80` |  |
| webserver.service.type | string | `"ClusterIP"` |  |
| webserver.tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.4.0](https://github.com/norwoodj/helm-docs/releases/v1.4.0)
