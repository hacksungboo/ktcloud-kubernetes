
### 기존 metallb clear

```bash
# custom resource definition 삭제 
kubectl get crd -o name | grep metallb | xargs kubectl delete

# metallb namespace 삭제 
kubectl delete namespace metallb-system --ignore-not-found=true

# metallb-webhook-configuration 삭제
kubectl delete ValidatingWebhookConfiguration metallb-webhook-configuration
```