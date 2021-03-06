---
title: docker/ucp upgrade
description: Upgrade the UCP components on this node
keywords: ucp, cli, upgrade
---

Upgrade the UCP cluster

## Usage

```
 docker container run --rm -it \
        --name ucp \
        -v /var/run/docker.sock:/var/run/docker.sock \
        docker/ucp \
        upgrade [command options]
```

## Description

This command upgrades the UCP running on this cluster.

Before performing an upgrade, you should perform a backup by using the
[backup](backup.md) command.

After upgrading UCP, go to the UCP web interface and confirm each node is
healthy and that all nodes have been upgraded successfully.


## Options

| Option                | Description                                                                                           |
|:----------------------|:------------------------------------------------------------------------------------------------------|
| `--debug, D`          | Enable debug mode                                                                                     |
| `--jsonlog`           | Produce json formatted output for easier parsing                                                      |
| `--interactive, i`    | Run in interactive mode and prompt for configuration values                                           |
| `--admin-username`    | The UCP administrator username                                                                        |
| `--admin-password`    | The UCP administrator password                                                                        |
| `--pull`              | Pull UCP images: `always`, when `missing`, or `never`                                                 |
| `--registry-username` | Username to use when pulling images                                                                   |
| `--registry-password` | Password to use when pulling images                                                                   |
| `--id`                | The ID of the UCP instance to upgrade                                                                 |
| `--host-address`      | Override the previously configured host address with this IP or network interface                     |
| `--force-minimums`    | Force the install/upgrade even if the system does not meet the minimum requirements                   |
| `--pod-cidr`          | Kubernetes cluster IP pool for the pods to allocated IP. The default IP pool is `192.168.0.0/16`.                 |
| `--nodeport-range`    | Allowed port range for Kubernetes services of type `NodePort`. The default port range is `32768-35535`.                   |
| `--cloud-provider`    | The cloud provider for the cluster                                                                    |
