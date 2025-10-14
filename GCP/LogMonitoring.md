# [Logs Explorer](https://cloud.google.com/logging/docs/view/logs-explorer-interface)
```bash
resource.type="k8s_node"
resource.labels.project_id="prod-eu-project"
resource.labels.location="europe-west1"
resource.labels.cluster_name="platform"
jsonPayload.reason="OOMKilling"
```
```bash
resource.type="k8s_container"
resource.labels.project_id="prod-eu-project"
resource.labels.location="europe-west1"
resource.labels.cluster_name="platform"
resource.labels.namespace_name="elb-system"
resource.labels.pod_name:"rate-limit-d58bcff68-"
severity=ERROR
```
```bash
resource.type="k8s_node"
resource.labels.project_id="owletcare-prod"
jsonPayload.reason="OOMKilling"
```
## [K8S](https://cloud.google.com/kubernetes-engine/docs/troubleshooting?_ga=2.167489592.-729104355.1657257577&_gac=1.126037375.1686680329.CjwKCAjwp6CkBhB_EiwAlQVyxfb_MroVHHAGumKP9r-vcl__jILiBKGHrjxNDJjt16rNZ04Gpa75-RoC58EQAvD_BwE#workload_issues)

```bash
gcloud container clusters get-credentials CLUSTER_NAME \
    --region=COMPUTE_REGION
```
```bash
kubectl get pods -n platform | grep token
```
```bash
kubectl get events -n platform | grep horizontal
```
```bash
kubectl describe pod rate-limit-d58bcff68-vkpvd | grep "Node:"
```
```bash
kubectl get pods -o wide | grep gke-platform-platform-68f090ea-cy4k | wc -l
```
```bash
kubectl describe pod rate-limit-d58bcff68-55ts6
```
```bash
kubectl describe pod rate-limit-d58bcff68-ss8bk
```
```bash
kubectl exec -it rate-limit-d58bcff68-ss8bk -- /bin/bash
```
```bash
kubectl get pod rate-limit-d58bcff68-ss8bk -o jsonpath='{.spec.containers[*].name}*
```
```bash
kubectl config set-context --current --namespace gloo-system
```
## PromQL Query
```bash
sum(avg_over_time(kubernetes_io:container_memory_limit_bytes{monitored_resource="k8s_container",location="us-central1",cluster_name="platform",namespace_name="platform",metadata_system_top_level_controller_type="Deployment",metadata_system_top_level_controller_name="trigger-wrapper-v1"}[${__interval}]))
```
