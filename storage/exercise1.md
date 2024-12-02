## Exercise 1

Create a persistent volume (PV) and a persistent volume claim (PVC).

### Requirements:
- Storage: 5Gi
- Access Modes: ReadWriteOnce.

<details>
  <summary><strong>Solution</strong></summary>

Persistent Volume:

```yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: pv-volume
spec:
  capacity:
    storage: 5Gi
  accessModes:
    - ReadWriteOnce
  hostPath:
    path: "/mnt/data"
```

Persistent Volume Claim:

```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvc-claim
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 5Gi
```

</details>
