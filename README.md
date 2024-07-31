### Galaan deployment

### Configuring Github

1. Set the repository secret for SSH_PRIVATE_KEY and VAULT_PASSWORD

2. Update the inventory file for the server ip

3. Clone this repository inside the server as `deploy` directory

4. Run the action to verify the configuration



#### Install ansible

```sh
sudo apt install ansible-core
```

#### Deploy backend

```sh
ansible-playbook playbook/deploy_be_dev.yml -i playbook/inventory.yml
```

#### Stop backend

```sh
ansible-playbook playbook/stop_be_dev.yml -i playbook/inventory.yml
```

#### Deploy frontend

```sh
ansible-playbook playbook/deploy_fe_dev.yml -i playbook/inventory.yml
```

#### Stop backend

```sh
ansible-playbook playbook/stop_fe_dev.yml -i playbook/inventory.yml
```
