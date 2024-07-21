# ansible

Ansible playbooks used in my daily activities.

1. Inital server install
2. Package update

```bash
ansible-playbook ~/ansible/ubuntu/update.yml --inventory-file ~/inventory -K
```

3. Expose docker service to portainer.io

```bash
ansible-playbook ~/ansible/docker/service/expose-docker-service.yml --inventory-file inventory -K
```

4. Restart hashicorp services

```bash
ansible-playbook ansible/hashicorp/restart_services.yml --inventory-file ~/inventory -K
```

5. Install qemu guest agent

```bash
ansible-playbook ~/ansible/qemu/install.yml --inventory-file ~/inventory --extra-vars 'target=some.server' -K
```