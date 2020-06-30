# Deploy NetQ to a Custom Topology

### Description

This playbook will deploy NetQ in a Custom Cumulus Air topology. The default setting in Air is to give the netq-ts server the IP address of 192.168.200.250. This value is set in the all.yaml group_vars file, in case it needs to be overridden.

1. Copy this playbook down to the OOB management server with the following command:

```
https://gitlab.com/nvidia-networking/systems-engineering/poc-support/deploy-netq-to-a-custom-topology
```

2. Either edit or copy your Ansible "hosts" file to the "hosts" file in the deploy-netq-to-a-custom-topology directory. Cumulus switch IP addresses should be under the [switches] section in the host file; Ubuntu 18.04 servers should be under the [servers] in the host file.

3. Run the following command:

```
ansible-playbook deploy-netq-to-a-custom-topology.yml
```

### Note:

I did not install the NetQ files onto the OOB server itself in this first revision. You will have to either log into the netq-ts server or to one of the switches to test and verify NetQ CLI connectivity. The NetQ GUI works from the Air console with the above the playbook, as well.
