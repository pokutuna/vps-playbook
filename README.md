vps-playbook
===

# How to Play
- put `hosts` like this
  ```
  [servers]
  your.server.domain.or.ip
  ```

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


# `pre_setup.yml`

- login with password authentication
- set hostname (optional)
  - vars: `hostname`
- put `~/.ssh/authorized_keys` from github
  - vars: `github_username`
- change ssh port  (optinal, default: `22`)
  - vars: `ssh_port`
- disable `PermitRootLogin`, `PasswordAuthentication`


```shell
# example
$ ansible-playbook -i "192.168.33.10," pre_setup.yml \
    --ask-pass \
    --extra-vars="hostname=oneetyan github_username=pokutuna ssh_port=8080"
```
