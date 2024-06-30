# clickhouse deployment

* exxute the below Yaml file in the below sequence order

```
kubectl apply -f pv-pvc.yml
kubectl apply -f configmap.yml
kubectl apply -f deploy.yml
kubectl apply -f service.yml
```

