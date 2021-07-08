# Deploy NetQ to a Custom Topology

### Note

See the 3.x release of this repo for older versions of NetQ:

```
https://gitlab.com/nvidia-networking/systems-engineering/poc-support/deploy-netq-to-a-custom-topology/-/releases
```

### Description

This will configure NetQ 4.x agents onto Cumulus Switches and Ubuntu 18.x servers within a custom Air topology.

1. Copy this playbook down to the OOB management server with the following command:

```
https://gitlab.com/nvidia-networking/systems-engineering/poc-support/deploy-netq-to-a-custom-topology
```

2. Either edit or copy your Ansible "hosts" file to the "hosts" file in the deploy-netq-to-a-custom-topology directory. Cumulus switch IP addresses should be under the [switches] section in the host file; Ubuntu 18.04 servers should be under the [servers] in the host file.

3. Run the following command from the "deploy-netq-to-a-custom-topology" directory:

```
ansible-playbook deploy-netq-to-a-custom-topology.yml
```
