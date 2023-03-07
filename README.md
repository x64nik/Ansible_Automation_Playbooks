
## Simple Format

```bash

.
├── inventory
│   └── hosts_vars
│       └── hosts.ini
├── roles
│   └── docker
│       └── tasks
│           └── main.yml
└── site.yml


```

## Simple Command

```bash

# without sudo password 
$ ansible-playbook --inventory ./inventory/hosts_vars/hosts.ini site.yml 


# with sudo password
$ ansible-playbook --inventory ./inventory/hosts_vars/hosts.ini site.yml --ask-become-pass

```



