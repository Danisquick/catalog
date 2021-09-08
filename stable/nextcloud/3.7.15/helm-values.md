# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| cronjob.annotations | object | `{}` |  |
| cronjob.failedJobsHistoryLimit | int | `5` |  |
| cronjob.schedule | string | `"*/5 * * * *"` |  |
| cronjob.successfulJobsHistoryLimit | int | `2` |  |
| env.NEXTCLOUD_ADMIN_PASSWORD | string | `"adminpass"` |  |
| env.NEXTCLOUD_ADMIN_USER | string | `"admin"` |  |
| env.TRUSTED_PROXIES | string | `"172.16.0.0/16"` |  |
| envFrom[0].configMapRef.name | string | `"nextcloudconfig"` |  |
| envTpl.POSTGRES_DB | string | `"{{ .Values.postgresql.postgresqlDatabase }}"` |  |
| envTpl.POSTGRES_USER | string | `"{{ .Values.postgresql.postgresqlUsername }}"` |  |
| envValueFrom.POSTGRES_HOST.secretKeyRef.key | string | `"host"` |  |
| envValueFrom.POSTGRES_HOST.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.POSTGRES_PASSWORD.secretKeyRef.key | string | `"postgresql-password"` |  |
| envValueFrom.POSTGRES_PASSWORD.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.REDIS_HOST.secretKeyRef.key | string | `"masterhost"` |  |
| envValueFrom.REDIS_HOST.secretKeyRef.name | string | `"rediscreds"` |  |
| envValueFrom.REDIS_HOST_PASSWORD.secretKeyRef.key | string | `"redis-password"` |  |
| envValueFrom.REDIS_HOST_PASSWORD.secretKeyRef.name | string | `"rediscreds"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"nextcloud"` |  |
| image.tag | string | `"22.1.1"` |  |
| initContainers[0].command[0] | string | `"sh"` |  |
| initContainers[0].command[1] | string | `"-c"` |  |
| initContainers[0].command[2] | string | `"until pg_isready -U nextcloud -h ${pghost} ; do sleep 2 ; done"` |  |
| initContainers[0].env[0].name | string | `"pghost"` |  |
| initContainers[0].env[0].valueFrom.secretKeyRef.key | string | `"plainhost"` |  |
| initContainers[0].env[0].valueFrom.secretKeyRef.name | string | `"dbcreds"` |  |
| initContainers[0].image | string | `"postgres:13.1"` |  |
| initContainers[0].imagePullPolicy | string | `"IfNotPresent"` |  |
| initContainers[0].name | string | `"init-postgresdb"` |  |
| initContainers[1].args[0] | string | `"if [ -f /var/www/html/occ ]; then if [ -n \"${NEXTCLOUD_TRUSTED_DOMAINS+x}\" ]; then echo \"setting trusted domains…\"; NC_TRUSTED_DOMAIN_IDX=1; for DOMAIN in $NEXTCLOUD_TRUSTED_DOMAINS ; do DOMAIN=$(echo \"$DOMAIN\" | sed -e 's/^[[:space:]]*//' -e 's/[[:space:]]*$//'); php /var/www/html/occ config:system:set trusted_domains $NC_TRUSTED_DOMAIN_IDX --value=$DOMAIN; NC_TRUSTED_DOMAIN_IDX=$(($NC_TRUSTED_DOMAIN_IDX+1)); done; fi; fi;"` |  |
| initContainers[1].command[0] | string | `"su"` |  |
| initContainers[1].command[1] | string | `"-p"` |  |
| initContainers[1].command[2] | string | `"www-data"` |  |
| initContainers[1].command[3] | string | `"-s"` |  |
| initContainers[1].command[4] | string | `"/bin/sh"` |  |
| initContainers[1].command[5] | string | `"-c"` |  |
| initContainers[1].envFrom[0].configMapRef.name | string | `"nextcloudconfig"` |  |
| initContainers[1].image | string | `"nextcloud:22.1.1"` |  |
| initContainers[1].name | string | `"injectconfig"` |  |
| initContainers[1].volumeMounts[0].mountPath | string | `"/var/www/html"` |  |
| initContainers[1].volumeMounts[0].name | string | `"data"` |  |
| persistence.data.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/var/www/html"` |  |
| persistence.data.size | string | `"100Gi"` |  |
| persistence.data.type | string | `"pvc"` |  |
| persistence.redismaster.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.redismaster.enabled | bool | `true` |  |
| persistence.redismaster.forceName | string | `"redismaster"` |  |
| persistence.redismaster.noMount | bool | `true` |  |
| persistence.redismaster.size | string | `"100Gi"` |  |
| persistence.redismaster.type | string | `"pvc"` |  |
| podSecurityContext.fsGroup | int | `33` |  |
| postgresql.enabled | bool | `true` |  |
| postgresql.existingSecret | string | `"dbcreds"` |  |
| postgresql.postgresqlDatabase | string | `"nextcloud"` |  |
| postgresql.postgresqlUsername | string | `"nextcloud"` |  |
| probes | object | See below | Probe configuration -- [[ref]](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/) |
| probes.liveness | object | See below | Liveness probe configuration |
| probes.liveness.spec | object | "/" | If a HTTP probe is used (default for HTTP/HTTPS services) this path is used |
| probes.readiness | object | See below | Redainess probe configuration |
| probes.readiness.spec | object | "/" | If a HTTP probe is used (default for HTTP/HTTPS services) this path is used |
| probes.startup | object | See below | Startup probe configuration |
| probes.startup.spec | object | "/" | If a HTTP probe is used (default for HTTP/HTTPS services) this path is used |
| redis.architecture | string | `"standalone"` |  |
| redis.auth.existingSecret | string | `"rediscreds"` |  |
| redis.auth.existingSecretPasswordKey | string | `"redis-password"` |  |
| redis.enabled | bool | `true` |  |
| redis.master.persistence.enabled | bool | `false` |  |
| redis.master.persistence.existingClaim | string | `"redismaster"` |  |
| redis.replica.persistence.enabled | bool | `false` |  |
| redis.replica.replicaCount | int | `0` |  |
| redis.volumePermissions.enabled | bool | `true` |  |
| service.hpb.enabled | bool | `true` |  |
| service.hpb.ports.hpb.enabled | bool | `true` |  |
| service.hpb.ports.hpb.port | int | `7867` |  |
| service.main.ports.main.port | int | `80` |  |
| strategy.type | string | `"Recreate"` |  |

All Rights Reserved - The TrueCharts Project