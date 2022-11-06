ansible-playbook -i inventory provisioning.yml
ansible-playbook -i inventory user_config.yml -e ansible_user=crash


ansible-playbook -i inventory user_config.yml -e ansible_user=crash --private-key=keyfilepath --start-at-task "Checkout dotfiles for user *"


--ask-pass --ask-become-pass


ansible-playbook -i diphda.uberspace.de, user_config.yml -e ansible_user=crash
ansible-playbook -i inventory user_config.yml -e ansible_user=crash --private-key=<keyfilepath> -k

ansible all -i localhost, -m debug -a "msg={{ lookup('password', '/dev/null chars=ascii_lowercase,digits length=5') }}"



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
