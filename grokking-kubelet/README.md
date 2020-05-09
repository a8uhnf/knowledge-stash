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