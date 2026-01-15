# Dev config

## Ansible

### Inventory
```ini
crydee ansible_host=<IP> ansible_user=root ansible_ssh_pass=<PASSWORD>
```

### Remote
`ansible-playbook -i inventory --limit crydee provisioning.yml`
`ansible-playbook -i inventory --limit crydee user_config.yml -e ansible_user=crash --private-key=<KEYFILEPATH> --start-at-task "Checkout dotfiles for user *"`

ANSIBLE_HOST_KEY_CHECKING=false ...


### Local
`ansible-playbook --connection=local -i 127.0.0.1, provisioning.yml --tags packages --become --ask-become-pass --step -v`
`ansible-playbook --connection=local -i 127.0.0.1, user_config.yml --start-at-task "Checkout dotfiles for user *"`


### Other
--ask-pass --ask-become-pass
-k

`ansible all -i localhost, -m debug -a "msg={{ lookup('password', '/dev/null chars=ascii_lowercase,digits length=5') }}"`


## Other commands

```bash
exa compile: podman run -it --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp rust cargo build --release


update-alternatives --get-selections

sudo update-alternatives --auto vim
sudo update-alternatives --config vim
sudo update-alternatives --set vim /usr/bin/nvim
sudo update-alternatives --remove vim /usr/bin/nvim

update-alternatives --display vim
sudo update-alternatives --install /usr/bin/vim vim /usr/bin/nvim 100

update-alternatives --display vi
sudo update-alternatives --install /usr/bin/vi vi /usr/bin/nvim 100
```
