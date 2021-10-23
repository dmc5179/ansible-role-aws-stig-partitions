ansible-role-aws-stig-partitions
=========

Ansible role to convert a RHEL 8 EC2 Instance to use STIG compliant partitions

Requirements
------------


Role Variables
--------------

| Variable                       | Default | Comments (type)                                                |
| :---                           | :---    | :---                                                           |
| aws_instance_id                | i-      | EC2 instance ID of the node to have its partitions resized     |
| temp_node_id                   | i-      | EC2 instance ID of the node used to repartition the node above |
| new_root_volume_size           | 100     | New size of the root volume in GBs                             |
| partitions.root.start          | 0%      | root parition start percentage                                 |
| partitions.root.end            | 30%     | root partition end percentage                                  |
| partitions.tmp.start           | 30%     | tmp  parition start percentage                                 |
| partitions.tmp.end             | 40%     | tmp partition end percentage                                   |
| partitions.var.start           | 40%     | var  parition start percentage                                 |
| partitions.var.end             | 50%     | var partition end percentage                                   |
| partitions.var_log_audit.start | 50%     | var_log_audit  parition start percentage                       |
| partitions.var_log_audit.end   | 60%     | var_log_audit partition end percentage                         |
| partitions.home.start          | 60%     | home  parition start percentage                                |
| partitions.home.end            | 100%    | home partition end percentage                                  |

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
