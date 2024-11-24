## Exercise 2

Schedule a pod on a specific node by applying a node selector.

### Requirements:
- Use the image: busybox
- Node must have label: `disktype=ssd`.

<details>
  <summary><strong>Solution</strong></summary>

Use the following YAML manifest:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: busybox-pod
spec:
  containers:
  - name: busybox
    image: busybox
    command: ["sh", "-c", "sleep 3600"]
  nodeSelector:
    disktype: ssd
```

</details>
