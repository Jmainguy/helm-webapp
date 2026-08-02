# webapp

![Version: 2.3.0](https://img.shields.io/badge/Version-2.3.0-informational?style=flat-square)

A helm chart for a standard webapp using istio ingress

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMaps | list | `[]` |  |
| env | list | `[]` |  |
| image.name | string | `"hey.soh.re"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"zot.soh.re"` |  |
| image.tag | string | `"v1.0.6"` |  |
| name | string | `"webapp"` |  |
| postgres.bootstrap.initdb.database | string | `"app"` |  |
| postgres.bootstrap.initdb.owner | string | `"app"` |  |
| postgres.enabled | bool | `false` |  |
| postgres.instances | int | `2` |  |
| postgres.name | string | `"postgres-cluster"` |  |
| postgres.storage.size | string | `"10Gi"` |  |
| redis.enabled | bool | `false` | Deploy an in-cluster Redis instance (Chainguard image). |
| redis.image.name | string | `"redis"` |  |
| redis.image.pullPolicy | string | `"IfNotPresent"` |  |
| redis.image.repository | string | `"cgr.dev/chainguard"` |  |
| redis.image.tag | string | `"latest"` |  |
| redis.injectEnv | bool | `false` | Set `REDIS_URL` on the webapp container when Redis is enabled. |
| redis.name | string | `"redis"` | Service and deployment name. |
| redis.persistence.enabled | bool | `true` | Persist Redis data under `/data`. |
| redis.persistence.size | string | `"1Gi"` | PVC size when persistence is enabled. |
| redis.port | int | `6379` | Redis port. |
| redis.replicas | int | `1` | Redis deployment replicas (use `1` for standalone). |
| redis.resources | object | `{}` |  |
| persistence | list | `[]` | List of persistence volumes. Each item: `name`, `mountPath`, and optionally `size` (new PVC), `existingClaim` (reuse PVC), `volumeName` (bind new PVC to existing PV). |
| replicaCount | int | `2` |  |
| resources | object | `{}` |  |
| secret.enabled | bool | `false` |  |
| secret.name | string | `"my-external-secret"` |  |
| service.name | string | `"hey-soh-re"` |  |
| service.port | int | `80` |  |
| service.targetPort | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
| virtualService.hosts[0] | string | `"hey.soh.re"` |  |

### Persistence

You can define multiple persistence volumes. For each item:

| Field | Required | Description |
|-------|----------|-------------|
| name | yes | Volume name (used as the Kubernetes volume name). |
| mountPath | yes | Path where the volume is mounted in the container. |
| size | no | Size for a new PVC (e.g. `"1Gi"`). Omit when using `existingClaim`. |
| existingClaim | no | Name of an existing PVC to use; no new PVC is created. |
| volumeName | no | When creating a new PVC, bind it to this existing PersistentVolume by name. |

Example: enable bundled Redis for live sync (e.g. Kanban `REDIS_URL`):

```yaml
redis:
  enabled: true
  injectEnv: true
```

Or set the URL manually:

```yaml
redis:
  enabled: true
env:
  REDIS_URL: redis://redis:6379/0
```

Example: create one new PVC and reuse an existing one:

```yaml
persistence:
  - name: data
    mountPath: /data
    size: 1Gi
  - name: cache
    mountPath: /cache
    existingClaim: my-existing-cache-pvc
```

