# k8s-monitor

1. node-exporter
kubectl create -f node-exporter.yaml

2. prometheus
kubectl create -f prometheus/rbac.yaml
kubectl create -f prometheus/configmap.yaml
kubectl create -f prometheus/deploy.yaml
kubectl create -f prometheus/svc.yaml

3. grafana
kubectl create -f grafana/grafana-deploy.yaml
kubectl create -f grafana/grafana-svc.yaml
kubectl create -f grafana/grafana-ing.yaml

===
fluentd, elasticsearch, kibana

ref
https://github.com/redhatxl/k8s-prometheus-grafana
