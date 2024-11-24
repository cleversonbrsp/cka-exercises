## Exercise 2

Inspect the etcd cluster health and back up the etcd data.

### Requirements:
- Access to the etcd pod
- kubectl installed

### Steps:
1. Check the health of etcd.
2. Back up the etcd database to a secure location.

<details>
  <summary><strong>Solution</strong></summary>

1. Use `kubectl exec -n kube-system etcd-master -- etcdctl endpoint health` to check health.
2. Run `kubectl exec -n kube-system etcd-master -- etcdctl snapshot save /var/lib/etcd/backup.db` to create a backup.

</details>
