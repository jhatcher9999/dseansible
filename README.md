# Manage DataStax Enterprise (DSE) Installation and Version Upgrade Using Ansible Playbook

It is not a trivial task to provision a large DSE cluster, to manage the key configuration item (e.g. dse.yaml, cassandra.yaml, etc.) changes, do version upgrade, and so on.  Historically (pre DSE 5.0), there is really no out-of-the-box method to manage these tasks automatically (as much as possible). Operationally, it is a time-consuming and error-prone job to manually run these tasks on every DSE node instance, not even to mention that for many cases, you also have to consider the task execution sequence among different DES nodes (e.g. DC by DC, rack by rack, seed vs. no-seed and so on).

Starting from DSE 5.0, OpsCenter 6.0 (as part of DSE 5.0 release) introduces a new component called Life Cycle Manager (LCM) that is designed for efficient installation and configuration of a DSE cluster through a web-browser based GUI. It aims to solve the above issue as an easy-to-use, flexible, out-of-the-box solution offered by DataStax. Although there are some limitations with the current version (OpsCenter 6.0.8 as the time of this writing), it is in general a good solution for automatic DSE cluster provisioning and configuration management. For more detailed information about this product, please reference to LCM's documentation page (https://docs.datastax.com/en/latest-opscenter/opsc/LCM/opscLCM.html). 

