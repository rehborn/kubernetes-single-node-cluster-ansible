# Kubernetes Single Node Cluster Ansible

full setup
```shell
ansible-playbook k8s/main.yml -l host
```

rollback:
```shell
ansible-playbook k8s/rollback.yml -l host
```


## Roles

### core

```shell
ansible-playbook k8s/main.yml -l host -t setup-core
```
tags: 
- `setup-kubernetes-core`
- `setup-storage-class`
- `setup-helm`
- `setup-ingress`
- `setup-calico`
- `setup-etcd`


### optional

```shell
ansible-playbook k8s/main.yml -l host -t setup-optional
```

tags:
- `cert_manager` (`jetstack`, `self_signed`)
- `metrics`
- `prometheus`
- `grafana`
- `loki`
- `fluentd`

- `status`
