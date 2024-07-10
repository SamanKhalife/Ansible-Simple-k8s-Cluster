# Ansible-Simple-k8s-Cluster

This Ansible playbook sets up a Kubernetes cluster with one master and two workers, designed for educational purposes. For production environments, it's recommended to use [Kubespray](https://github.com/kubernetes-sigs/kubespray).

## Prerequisites

1. Set up SSH configuration (based on RSA keys) between the master and worker nodes.
2. Install Ansible on the master node (Ansible makes changes locally to the master node).

## Steps to Set Up the Cluster

### 1. Configure Host Variables

Update the default values in the [host_vars](https://github.com/SamanKhalife/Ansible-Simple-k8s-Cluster/tree/main/host_vars) directory with your master and worker nodes' IPs or domains.

Verify the connection:
```bash
ansible all -m ping
```

### 2. Run the Playbook

Navigate to the playbook directory and execute the playbook:
```bash
cd playbooks
ansible-playbook cluster.yml
```

### 3. Be Patient

Wait for a few minutes for the Kubernetes cluster to be set up and running.

## Additional Information

For more advanced or production-ready setups, consider using [Kubespray](https://github.com/kubernetes-sigs/kubespray).
