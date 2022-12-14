# bottlerocket-brupop

![Version: 0.4.5](https://img.shields.io/badge/Version-0.4.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.1](https://img.shields.io/badge/AppVersion-1.16.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Get Repo Info
```console
helm repo add bottlerocket-update-operator https://franklinpashok.github.io/bottlerocket-update-operator/
helm repo update
```

## Installing the Chart
To install the chart with the release name my-release:

```console
helm install my-brupop bottlerocket-update-operator/bottlerocket-update-operator
```

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```console
helm uninstall my-brupop
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"public.ecr.aws/bottlerocket/bottlerocket-update-operator"` |  |
| image.tag | string | `"v0.2.2"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| namespace | string | `"brupop-bottlerocket"` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| rbacagent.create | bool | `true` |  |
| rbacagent.extraClusterRoleRules | list | `[]` |  |
| rbacagent.extraRoleRules | list | `[]` |  |
| rbacagent.name | string | `"brupop-agent-role"` |  |
| rbacagent.namespaced | bool | `false` |  |
| rbacapiserver.create | bool | `true` |  |
| rbacapiserver.extraClusterRoleRules | list | `[]` |  |
| rbacapiserver.extraRoleRules | list | `[]` |  |
| rbacapiserver.name | string | `"brupop-apiserver"` |  |
| rbacapiserver.namespaced | bool | `false` |  |
| rbaccontroller.create | bool | `true` |  |
| rbaccontroller.extraClusterRoleRules | list | `[]` |  |
| rbaccontroller.extraRoleRules | list | `[]` |  |
| rbaccontroller.name | string | `"brupop-controller-role"` |  |
| rbaccontroller.namespaced | bool | `false` |  |
| replicaCountController | int | `1` |  |
| replicaCountapiServer | int | `3` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| serviceaccountagent.annotations | object | `{}` |  |
| serviceaccountagent.create | bool | `true` |  |
| serviceaccountagent.name | string | `"brupop-agent-service-account"` |  |
| serviceaccountapiserver.annotations | object | `{}` |  |
| serviceaccountapiserver.create | bool | `true` |  |
| serviceaccountapiserver.name | string | `"brupop-apiserver-service-account"` |  |
| serviceaccountcontroller.annotations | object | `{}` |  |
| serviceaccountcontroller.create | bool | `true` |  |
| serviceaccountcontroller.name | string | `"brupop-controller-service-account"` |  |
| serviceapiserver.annotations | object | `{}` |  |
| serviceapiserver.appProtocol | string | `""` |  |
| serviceapiserver.enabled | bool | `true` |  |
| serviceapiserver.labels | object | `{}` |  |
| serviceapiserver.name | string | `"brupop-apiserver"` |  |
| serviceapiserver.port | int | `443` |  |
| serviceapiserver.portName | string | `"service"` |  |
| serviceapiserver.targetPort | int | `8443` |  |
| serviceapiserver.type | string | `"ClusterIP"` |  |
| servicecontroller.enabled | bool | `true` |  |
| servicecontroller.name | string | `"brupop-controller-server"` |  |
| servicecontroller.port | int | `80` |  |
| servicecontroller.targetPort | int | `8080` |  |
| servicecontroller.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
