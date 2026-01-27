# keycloak

![Version: 0.14.0](https://img.shields.io/badge/Version-0.14.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 26.5.2](https://img.shields.io/badge/AppVersion-26.5.2-informational?style=flat-square)

Open Source Identity and Access Management Solution

**Homepage:** <https://www.keycloak.org>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| CloudPirates GmbH & Co. KG | <hello@cloudpirates.io> | <https://www.cloudpirates.io> |

## Source Code

* <https://github.com/CloudPirates-io/helm-charts/tree/main/charts/keycloak>
* <https://github.com/keycloak/keycloak>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| oci://registry-1.docker.io/cloudpirates | common | 2.x.x |
| oci://registry-1.docker.io/cloudpirates | mariadb | 0.4.x |
| oci://registry-1.docker.io/cloudpirates | postgres | 0.9.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| cache.configFile | string | `""` |  |
| cache.stack | string | `"local"` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| containerSecurityContext.runAsGroup | int | `1001` |  |
| containerSecurityContext.runAsNonRoot | bool | `true` |  |
| containerSecurityContext.runAsUser | int | `1001` |  |
| database.existingSecret | string | `""` |  |
| database.host | string | `""` |  |
| database.jdbcParams | string | `""` |  |
| database.name | string | `"keycloak"` |  |
| database.password | string | `""` |  |
| database.port | string | `""` |  |
| database.schema | string | `""` |  |
| database.secretKeys.passwordKey | string | `"db-password"` |  |
| database.secretKeys.usernameKey | string | `"db-username"` |  |
| database.type | string | `"postgres"` |  |
| database.urlProperties | string | `""` |  |
| database.username | string | `"keycloak"` |  |
| extraEnvVars | list | `[]` |  |
| extraEnvVarsSecret | string | `""` |  |
| extraInitContainers | list | `[]` |  |
| extraObjects | list | `[]` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| features.disabled | list | `[]` |  |
| features.enabled | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| image.command | string | `"/opt/keycloak/bin/kc.sh"` |  |
| image.imagePullPolicy | string | `"Always"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"keycloak/keycloak"` |  |
| image.tag | string | `"26.5.2@sha256:fb31a59deb46f746f2aaa25adc5da39ceccac4fd22d36a519562b0bf02e8df20"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"keycloak.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| initContainers.waitForMariadb.image | string | `""` |  |
| initContainers.waitForMariadb.pullPolicy | string | `"IfNotPresent"` |  |
| initContainers.waitForMariadb.registry | string | `""` |  |
| initContainers.waitForMariadb.repository | string | `"mariadb"` |  |
| initContainers.waitForMariadb.resources.limits.cpu | string | `"100m"` |  |
| initContainers.waitForMariadb.resources.limits.memory | string | `"64Mi"` |  |
| initContainers.waitForMariadb.resources.requests.cpu | string | `"50m"` |  |
| initContainers.waitForMariadb.resources.requests.memory | string | `"32Mi"` |  |
| initContainers.waitForMariadb.tag | string | `"12.0.2@sha256:03a03a6817bb9eaa21e5aed1b734d432ec3f80021f5a2de1795475f158217545"` |  |
| initContainers.waitForPostgres.image | string | `""` |  |
| initContainers.waitForPostgres.pullPolicy | string | `"IfNotPresent"` |  |
| initContainers.waitForPostgres.registry | string | `""` |  |
| initContainers.waitForPostgres.repository | string | `"postgres"` |  |
| initContainers.waitForPostgres.resources.limits.cpu | string | `"100m"` |  |
| initContainers.waitForPostgres.resources.limits.memory | string | `"64Mi"` |  |
| initContainers.waitForPostgres.resources.requests.cpu | string | `"50m"` |  |
| initContainers.waitForPostgres.resources.requests.memory | string | `"32Mi"` |  |
| initContainers.waitForPostgres.tag | string | `"17.6@sha256:e6a4209d1a4893f2df3bdcde58f8926c3c929c4d51df90990ed1b36d83c1382a"` |  |
| keycloak.adminPassword | string | `""` |  |
| keycloak.adminUser | string | `"admin"` |  |
| keycloak.existingSecret | string | `""` |  |
| keycloak.extraArgs | list | `[]` |  |
| keycloak.hostname | string | `""` |  |
| keycloak.hostnameAdmin | string | `""` |  |
| keycloak.hostnameBackchannel | string | `""` |  |
| keycloak.hostnameStrict | bool | `false` |  |
| keycloak.httpEnabled | bool | `true` |  |
| keycloak.httpPort | int | `8080` |  |
| keycloak.httpRelativePath | string | `"/"` |  |
| keycloak.httpsEnabled | bool | `false` |  |
| keycloak.httpsPort | int | `8443` |  |
| keycloak.production | bool | `false` |  |
| keycloak.proxyHeaders | string | `""` |  |
| keycloak.proxyProtocolEnabled | bool | `false` |  |
| keycloak.proxyTrustedAddresses | string | `""` |  |
| keycloak.secretKeys.adminPasswordKey | string | `"admin-password"` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `30` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| mariadb.auth.database | string | `"keycloak"` |  |
| mariadb.auth.password | string | `""` |  |
| mariadb.auth.rootPassword | string | `""` |  |
| mariadb.auth.username | string | `""` |  |
| mariadb.enabled | bool | `false` |  |
| metrics.enabled | bool | `false` |  |
| metrics.service.annotations | object | `{}` |  |
| metrics.service.labels | object | `{}` |  |
| metrics.service.port | int | `9000` |  |
| metrics.service.targetPort | string | `"http-metrics"` |  |
| metrics.service.type | string | `"ClusterIP"` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.annotations | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `"30s"` |  |
| metrics.serviceMonitor.jobLabel | string | `""` |  |
| metrics.serviceMonitor.metricRelabelings | list | `[]` |  |
| metrics.serviceMonitor.namespace | string | `""` |  |
| metrics.serviceMonitor.relabelings | list | `[]` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `""` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `false` |  |
| persistence.existingClaim | string | `""` |  |
| persistence.size | string | `"1Gi"` |  |
| persistence.storageClass | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.fsGroup | int | `1001` |  |
| postgres.auth.database | string | `"keycloak"` |  |
| postgres.auth.password | string | `""` |  |
| postgres.auth.username | string | `""` |  |
| postgres.enabled | bool | `true` |  |
| preserveProviders | bool | `false` |  |
| preserveThemes | bool | `false` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `30` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `5` |  |
| realm.configFile | string | `""` |  |
| realm.existingSecret | string | `""` |  |
| realm.import | bool | `false` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.annotations | object | `{}` |  |
| service.httpPort | int | `8080` |  |
| service.httpTargetPort | int | `8080` |  |
| service.httpsPort | int | `8443` |  |
| service.httpsTargetPort | int | `8443` |  |
| service.trafficDistribution | string | `""` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `false` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| startupProbe.enabled | bool | `true` |  |
| startupProbe.failureThreshold | int | `60` |  |
| startupProbe.initialDelaySeconds | int | `30` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `5` |  |
| tls.certManager.annotations | object | `{}` |  |
| tls.certManager.commonName | string | `""` |  |
| tls.certManager.dnsNames | list | `[]` |  |
| tls.certManager.duration | string | `""` |  |
| tls.certManager.enabled | bool | `false` |  |
| tls.certManager.ipAddresses | list | `[]` |  |
| tls.certManager.issuerRef.group | string | `"cert-manager.io"` |  |
| tls.certManager.issuerRef.kind | string | `"ClusterIssuer"` |  |
| tls.certManager.issuerRef.name | string | `""` |  |
| tls.certManager.renewBefore | string | `""` |  |
| tls.certManager.secretName | string | `""` |  |
| tls.certManager.usages[0] | string | `"digital signature"` |  |
| tls.certManager.usages[1] | string | `"key encipherment"` |  |
| tls.certificateFile | string | `"/opt/keycloak/certs/tls.crt"` |  |
| tls.certificateKeyFile | string | `"/opt/keycloak/certs/tls.key"` |  |
| tls.enabled | bool | `false` |  |
| tls.existingSecret | string | `""` |  |
| tls.truststoreEnabled | bool | `false` |  |
| tls.truststoreExistingSecret | string | `""` |  |
| tls.truststoreExistingSecretKey | string | `"truststore.jks"` |  |
| tls.truststoreFile | string | `"/opt/keycloak/truststore/truststore.jks"` |  |
| tls.truststorePassword | string | `""` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
