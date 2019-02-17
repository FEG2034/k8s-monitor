# k8s-monitor

minikube

**connect**

eval $(minikube docker-env)

**stop**

eval $(minikube docker-env -u)


1. node-exporter
   * kubectl create -f node-exporter.yaml

2. prometheus
   * kubectl create -f prometheus/rbac.yaml
   * kubectl create -f prometheus/configmap.yaml
   * kubectl create -f prometheus/deploy.yaml
   * kubectl create -f prometheus/svc.yaml

3. grafana
   * kubectl create -f grafana/grafana-deploy.yaml
   * kubectl create -f grafana/grafana-svc.yaml
   * kubectl create -f grafana/grafana-ing.yaml

**Check node-exporter**
   * minikube ip:31672/metrics

**Check prometheus target**
   * minikube ip:30003/target

**Check grafana**
   * minikube ip:/port
   * default username/password is admin
   * add Data Sources
   * import Dashbosrd >> 315 Template
---
fluentd, elasticsearch, kibana

ref
https://github.com/redhatxl/k8s-prometheus-grafana
