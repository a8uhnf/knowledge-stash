# Grokking kubelet
---
### See kubelet config
1. ssh into node
2. systemctl cat kubelet  

### Follow kubelet logs
- journalctl -flu kubelet

### Run static pods
- downloads pod's manifests into `/etc/kubernetes/manifests`
- this pod isn't maintained by kube-apiserver. Its completely maintained by kubelet.

### check kube apiserver's etcd 
- download `https://git.io/etcdclient.yaml` in `/etc/kubernetes/manifests`. only in control plane.
- etcdctl get "" --from-key --keys-only

### kubelet expressed commands
- kubectl cp, logs, exec, attach