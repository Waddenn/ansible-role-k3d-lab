# ansible-role-k3d-lab

Role Ansible pour deployer un cluster k3d local (1 server, 1 agent) et publier un NGINX personnalise sur un NodePort.

## Variables

- `k3d_cluster_name` (defaut: `k3d-lab`)
- `k3d_manifest_path` (defaut: `/tmp/nginx.yaml`)
- `k3d_nodeport` (defaut: `30080`)
- `k3d_welcome_message` (defaut: `Bienvenue dans le k3d LAB`)

## Exemple de playbook

```yaml
---
- name: Tester le role Waddenn.k3d_lab
  hosts: localhost
  connection: local
  become: true
  roles:
    - Waddenn.k3d_lab
```
