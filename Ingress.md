
## Wildcard path
```yaml
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: gateway
  annotations:
    kubernetes.io/ingress.class: "istio"
spec:
  rules:
  - host: store.minikube.io
    http:
      paths:
      - path: /.*
        backend:
          serviceName: store-fe
          servicePort: 8080
 ```
