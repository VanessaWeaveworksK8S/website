---
title: Controller Options
linkTitle: Controller Options
description: "Controller command flags and defaults."
weight: 1000
---

To customise the controller options at install time,
please see the [bootstrap cheatsheet](../../cheatsheets/bootstrap.md).

## Flags

| Name                                  | Type     | Description                                                                                                                                            |
|---------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `--concurrent`                        | int      | The number of concurrent kustomize reconciles. (default 4)                                                                                             |
| `--default-service-account`           | string   | Default service account used for impersonation.                                                                                                        |
| `--enable-leader-election`            | boolean  | Enable leader election for controller manager. Enabling this will ensure there is only one active controller manager.                                  |
| `--events-addr`                       | string   | The address of the events receiver.                                                                                                                    |
| `--health-addr`                       | string   | The address the health endpoint binds to. (default ":9440")                                                                                            |
| `--http-retry`                        | int      | The maximum number of retries when failing to fetch artifacts over HTTP. (default 9)                                                                   |
| `--insecure-kubeconfig-exec`          | boolean  | Allow use of the user.exec section in kubeconfigs provided for remote apply.                                                                           |
| `--insecure-kubeconfig-tls`           | boolean  | Allow that kubeconfigs provided for remote apply can disable TLS verification.                                                                         |
| `--kube-api-burst`                    | int      | The maximum burst queries-per-second of requests sent to the Kubernetes API. (default 100)                                                             |
| `--kube-api-qps`                      | float32  | The maximum queries-per-second of requests sent to the Kubernetes API. (default 50)                                                                    |
| `--leader-election-lease-duration`    | duration | Interval at which non-leader candidates will wait to force acquire leadership (duration string). (default 35s)                                         |
| `--leader-election-release-on-cancel` | boolean  | Defines if the leader should step down voluntarily on controller manager shutdown. (default true)                                                      |
| `--leader-election-renew-deadline`    | duration | Duration that the leading controller manager will retry refreshing leadership before giving up (duration string). (default 30s)                        |
| `--leader-election-retry-period`      | duration | Duration the LeaderElector clients should wait between tries of actions (duration string). (default 5s)                                                |
| `--log-encoding`                      | string   | Log encoding format. Can be 'json' or 'console'. (default "json")                                                                                      |
| `--log-level`                         | string   | Log verbosity level. Can be one of 'trace', 'debug', 'info', 'error'. (default "info")                                                                 |
| `--max-retry-delay`                   | duration | The maximum amount of time for which an object being reconciled will have to wait before a retry. (default 15m0s)                                      |
| `--metrics-addr`                      | string   | The address the metric endpoint binds to. (default ":8080")                                                                                            |
| `--min-retry-delay`                   | duration | The minimum amount of time for which an object being reconciled will have to wait before a retry. (default 750ms)                                      |
| `--no-cross-namespace-refs`           | boolean  | When set to true, references between custom resources are allowed only if the reference and the referee are in the same namespace.                     |
| `--no-remote-bases`                   | boolean  | Disallow remote bases usage in Kustomize overlays. When this flag is enabled, all resources must refer to local files included in the source artifact. |
| `--requeue-dependency`                | duration | The interval at which failing dependencies are reevaluated. (default 30s)                                                                              |
| `--watch-all-namespaces`              | boolean  | Watch for custom resources in all namespaces, if set to false it will only watch the runtime namespace. (default true)                                 |
