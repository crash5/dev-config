ansible-playbook -i inventory provisioning.yml
ansible-playbook -i inventory user_config.yml -e ansible_user=crash


ansible-playbook -i inventory user_config.yml -e ansible_user=crash --private-key=keyfilepath --start-at-task "Checkout dotfiles for user *"



ansible-playbook -i diphda.uberspace.de, user_config.yml -e ansible_user=crash
ansible-playbook -i inventory user_config.yml -e ansible_user=crash --private-key=keyfilepath -k

ansible all -i localhost, -m debug -a "msg={{ lookup('password', '/dev/null chars=ascii_lowercase,digits length=5') }}"