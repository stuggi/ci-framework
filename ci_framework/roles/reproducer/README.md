# reproducer
Role to deploy close to CI layout on a hypervisor.

## Privilege escalation
None

## Parameters
* `cifmw_reproducer_basedir`: (String) Base directory. Defaults to `cifmw_basedir`, which defaults to `~/ci-framework-data`.
* `cifmw_reproducer_ctl_ip4`: (String) IPv4 address for ansible controller on the *private* interface. Defaults to 192.168.122.10.
* `cifmw_reproducer_ctl_gw4`: (String) IPv4 gateway for ansible controller on the *private* interface. Defaults to 192.168.122.1.
* `cifmw_reproducer_crc_ip4`: (String) IPv4 address for CRC node on the *private* interface. Defaults to 192.168.122.11.
* `cifmw_reproducer_crc_gw4`: (String) IPv4 gateway for CRC node on the *private* interface. Defaults to 192.168.122.1.
* `cifmw_reproducer_kubecfg`: (String) Path to the CRC kubeconfig file. Defaults to the image_local_dir defined in the cifmw_libvirt_manager_configuration dict.
* `cifmw_reproducer_repositories`: (List[mapping]) List of repositories you want to synchronize from your local machine to the ansible controller.
* `cifmw_reproducer_run_job`: (Bool) Run actual CI job. Defaults to `true`.
* `cifmw_reproducer_params`: (Dict) Specific parameters you want to pass to the reproducer. Defaults to `{}`.
* `cifmw_reproducer_private_nic`: (String) Private NIC for compute and controller. Defaults to `eth1`.
* `cifmw_reproducer_crc_private_nic`: (String) Private NIC for CRC node. Defaults to `enp2s0`.
* `cifmw_reproducer_dns_servers`: List of dns servers which should be used by the CRC VM as upstream dns servers. Defaults to 1.1.1.1, 8.8.8.8.

## Warning
This role isn't intended to be called outside of the `reproducer.yml` playbook.

## Examples
Please follow the [documentation about the overall "reproducer" feature](https://ci-framework.readthedocs.io/en/latest/cookbooks/reproducer.html).
