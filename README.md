
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

/


```

## Simple Command

```bash

# without sudo password 
$ ansible-playbook --inventory ./inventory/hosts_vars/hosts.ini site.yml 


# with sudo password
$ ansible-playbook --inventory ./inventory/hosts_vars/hosts.ini site.yml --ask-become-pass

```

## Add SSH key to target

```bash

# Generate SSH Key
$ ssh-keygen
> ... (add path and name of key and all)

# copy .pub to target authorized_keys 
$ ssh-copy-id -i <path_to_new_generated_key.pub> uname@<ip>

# ADD ssh key in ansible hosts file
# Example
[hosts-name]
192.168.0.108 ansible_ssh_private_key_file=<path_to_privet-key>

# Ezz ;)

```
