Ansible Role: Kubernetes Create Cluster
=========

Create a Kubernetes cluster using kubeadm.

Requirements
------------

Kubernetes binaries should already be installed (kubelet, kubeadm, kubectl).

Role Variables
--------------

None

Dependencies
------------

This playbook depends on the `jedimt.ansible-role-kubernetes-prep` role having been executed on the hosts prior to running.

Example Playbook
----------------

        # ===========================================================================
        # Create Kubernetes cluster
        # ===========================================================================
        - name: Create Kubernetes cluster
          hosts: k8s_master
          tags: play_create_k8s_cluster

        vars_files:
          # Ansible vault with all required passwords
          - "../../credentials.yml"

        roles:
          - ansible-role-kubernetes-create-cluster

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com
