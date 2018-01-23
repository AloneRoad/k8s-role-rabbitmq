# Ansible Role: RabbitMQ HA for Kubernetes

Ansible role to install RabbitMQ HA on Kubernetes.

## Dependencies

`kubectl` needs to be installed on the host  targeted by the role.

## Example Playbook

```yaml
- hosts: kube-master
  run_once: true
  vars:
    rabbitmq_username: foo
    rabbitmq_password: bar
  roles:
    - role: rabbitmq
```

Use `run_once` to run the role on only one available master in the cluster.
