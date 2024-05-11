# ocp-cluster-upgrade-gitops-way

https://docs.openshift.com/container-platform/4.14/rest_api/config_apis/clusterversion-config-openshift-io-v1.html#spec

| Property | Type | Description |
| -- | -- | -- |
| desiredUpdate | object | desiredUpdate is an optional field that indicates the desired value of the cluster version. Setting this value will trigger an upgrade (if the current version does not match the desired version). The set of recommended update values is listed as part of available updates in status, and setting values outside that range may cause the upgrade to fail. Some of the fields are inter-related with restrictions and meanings described here. 1. image is specified, version is specified, architecture is specified. API validation error. 2. image is specified, version is specified, architecture is not specified. You should not do this. version is silently ignored and image is used. 3. image is specified, version is not specified, architecture is specified. API validation error. 4. image is specified, version is not specified, architecture is not specified. image is used. 5. image is not specified, version is specified, architecture is specified. version and desired architecture are used to select an image. 6. image is not specified, version is specified, architecture is not specified. version and current architecture are used to select an image. 7. image is not specified, version is not specified, architecture is specified. API validation error. 8. image is not specified, version is not specified, architecture is not specified. API validation error. If an upgrade fails the operator will halt and report status about the failing component. Setting the desired update value back to the previous version will cause a rollback to be attempted. Not all rollbacks will succeed. |

## License

This work is under [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the [LICENSE](LICENSE) file for more details.
