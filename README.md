Role Name
=========

The implementation for the Advanced Ansible Homework.

Requirements
------------

OpenStack: cloud-user
AWS: ec2-user

Role Variables
--------------
```
[root@control 0 ~/nextgen_ansible_advanced_homework master ⭑|✚1…1]# tree
.
├── ansible.cfg
├── aws_creds.yml
├── aws_provision.yml
├── aws_status_check.yml
├── grading-script.yml
├── labrc
├── Readme.adoc
├── README.md
├── roles
│   ├── app-tier
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── index.html.j2
│   │   └── vars
│   │       └── main.yml
│   ├── base-config
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   ├── index.html.j2
│   │   │   └── repos_template.j2
│   │   └── vars
│   │       └── main.yml
│   ├── config-tower
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── files
│   │   │   ├── inventory_vars.json
│   │   │   ├── read_only.json
│   │   │   └── workstation_creds.json
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── README.md
│   │   ├── tasks
│   │   │   ├── ec2_dynamic.yml
│   │   │   ├── job_template.yml
│   │   │   ├── main.yml
│   │   │   ├── post-config-tower.yml
│   │   │   ├── pre-config-tower.yml
│   │   │   └── workflow_template.yml
│   │   ├── templates
│   │   │   ├── aws_jq_vars.yml
│   │   │   ├── tower_cli.j2
│   │   │   ├── tower_info.yml
│   │   │   └── workflow.j2
│   │   ├── tests
│   │   │   ├── inventory
│   │   │   └── test.yml
│   │   └── vars
│   │       └── main.yml
│   ├── db-tier
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── pg_hba.conf.j2
│   │   └── vars
│   │       └── main.yml
│   ├── lb-tier
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── haproxy.cfg.j2
│   │   └── vars
│   │       └── main.yml
│   ├── osp-facts
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── README.md
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── tests
│   │   │   ├── inventory
│   │   │   └── test.yml
│   │   └── vars
│   │       └── main.yml
│   ├── osp-instance-delete
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── README.md
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── tests
│   │   │   ├── inventory
│   │   │   └── test.yml
│   │   └── vars
│   │       └── main.yml
│   ├── osp-servers
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── README.md
│   │   ├── tasks
│   │   │   ├── app1.yml
│   │   │   ├── app2.yml
│   │   │   ├── db.yml
│   │   │   ├── frontend.yml
│   │   │   └── main.yml
│   │   ├── tests
│   │   │   ├── inventory
│   │   │   └── test.yml
│   │   └── vars
│   │       └── main.yml
│   ├── osp-setup
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── meta
│   │   │   └── main.yml
│   │   ├── README.md
│   │   ├── tasks
│   │   │   ├── create-flavor.yml
│   │   │   ├── create-image.yml
│   │   │   ├── create-keypair.yml
│   │   │   ├── create-network.yml
│   │   │   ├── create-sg.yml
│   │   │   └── main.yml
│   │   ├── tests
│   │   │   ├── inventory
│   │   │   └── test.yml
│   │   └── vars
│   │       └── main.yml
│   └── setup-workstation
│       ├── defaults
│       │   └── main.yml
│       ├── handlers
│       │   └── main.yml
│       ├── meta
│       │   └── main.yml
│       ├── README.md
│       ├── tasks
│       │   ├── create-flavor.yml
│       │   ├── create-image.yml
│       │   ├── create-keypair.yml
│       │   ├── create-network.yml
│       │   ├── create-sg.yml
│       │   ├── main.yml
│       │   └── pre-tasks.yml
│       ├── tests
│       │   ├── inventory
│       │   └── test.yml
│       └── vars
│           └── main.yml
├── script-report-20210424.txt
├── site-3tier-app.yml
├── site-config-tower.yml
├── site-install-isolated-node.yaml
├── site-osp-delete.yml
├── site-osp-instances.yml
├── site-setup-prereqs.yaml
├── site-setup-workstation.yml
├── site-smoke-osp.yml
└── site-smoketest-aws.yml
```

Dependencies
------------
Above

Instructions
------------
Full instructions, please see https://www.opentlc.com/download/ansible_bootcamp/course/10_Assignment/10_Final_Lab.html#_provision_production_environment


Example Playbook
----------------
```
[root@control 0 ~/nextgen_ansible_advanced_homework master ⭑|✔]# ansible-playbook grading-script.yml -vv 2>&1 | tee script-report-20210424.txt


- hosts: localhost
  gather_facts: false
  vars:
    OSP_GUID: "{{ lookup('env','OSP_GUID') }}"
    OSP_DOMAIN: "{{ lookup('env','OSP_DOMAIN') }}"
    TOWER_GUID: "{{ lookup('env','TOWER_GUID') }}"
  tasks:
  - name: Create In-memory Inventory
    add_host: 
      name: workstation-{{ OSP_GUID }}.{{ OSP_DOMAIN }}
      group: workstation
      ansible_ssh_private_key_file: ~/.ssh/openstack.pem
      ansible_ssh_user: cloud-user
```

Known Issues
------------
During the AWS provisioning, the configuration /etc/haproxy/haproxy.cfg from the frontend1 needs to be updated to use the internal IP addresses. 
For the AWS Cred stage, make sure to use the correct public and private ssh keys for the opentlc key. 

License
-------

BSD

Author Information
------------------
Sam Sun 
