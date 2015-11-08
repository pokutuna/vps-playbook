vps-playbook
===

# How to Run
```shell
$ ansible-galaxy install -r requriements.yml
$ ansible-playbook site.yml
```

# System
- Working for Ubuntu 14.04(and maybe also Debian)

# Referencing Environment Variables
- `MACKEREL_API_KEY`: setup for mackerel-agent
- `IM_KAYAC_USERNAME`: notify process events under the supervisord by im-kayac
- `IM_KAYAC_PASSWORD`: authenticate im-kayac api (optional)
