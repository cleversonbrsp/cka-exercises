## Exercise 1

Expose an application externally using an Ingress.

### Requirements:
- App: nginx
- Path: `/`
- Port: 80.

<details>
  <summary><strong>Solution</strong></summary>

Use the following Ingress manifest:

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: nginx-ingress
spec:
  rules:
  - http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: nginx-service
            port:
              number: 80
```

</details>
