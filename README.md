[![Build Status](https://drone.kiwi-labs.net/api/badges/Diesel-Net/kibana/status.svg)](https://drone.kiwi-labs.net/Diesel-Net/kibana)

# kibana
Kibana WebUI deployed for our EFK stack

## Notes
- [Kibana configuration settings](https://www.elastic.co/guide/en/kibana/current/settings.html)
  - All settings from config suppposedly can be mapped to environment variables instead, although they don't provide a complete list anywhere it seems like

## Installing External Dependencies
Ansible `2.10.3` was used at the time of this writing.
```bash
ansible-galaxy install -r .ansible/roles/requirements.deploy.yaml -p .ansible/roles --force
```

## Deploy
```bash
ansible-playbook .ansible/deploy.yaml -i .ansible/inventories/production/hosts --vault-id ~/.tokens/vault.txt
```
