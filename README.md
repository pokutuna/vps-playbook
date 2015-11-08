vps-playbook
===

# How to Play
```shell
$ ansible-galaxy install -r requriements.yml
$ ansible-playbook site.yml
```

## `pre_setup.yml`
- login with password authentication
- set hostname
- put authorized_keys
- basic ssh config

```shell
# example
$ ansible-playbook -i "192.168.33.10," pre_setup.yml \
    --ask-pass --extra-vars="hostname=oneetyan ssh_port=8080"
```

# System
- Working for Ubuntu 14.04(and maybe also Debian)

# Referencing Environment Variables
- `MACKEREL_API_KEY`: setup for mackerel-agent
- `IM_KAYAC_USERNAME`: notify process events under the supervisord by im-kayac
- `IM_KAYAC_PASSWORD`: authenticate im-kayac api (optional)
