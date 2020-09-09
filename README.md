# Kubernetes 101
## DEPLOYMENTS
##### Information of Deployments and POD
```
kubectl get deployment
kubectl get pod
kubectl describe deployment [DEPLOYMENT NAME]
kubectl describe pod [POD NAME]
kubectl kubectl scale --replicas=3 deployment [DEPLOYMENT NAME]
```
##### Deployment Scale
```
kubectl kubectl scale --replicas=3 deployment [DEPLOYMENT NAME]
```
## SERVICES
##### Information of Services
```
kubectl get svc
kubectl describe svc [SERVICE NAME]
```
##### Expose and Forward Service from ClusterIP
```
kubectl proxy --port=8080
curl -v http://localhost:8080/api/v1/namespaces/default/services/[SERVICE NAME]/proxy/[ROOTCONTEXT]
kubectl port-forward [POD NAME] [EXTERNAL PORT]:[INTERNAL PORT]
curl http://localhost:8080/status/200
```
##### Ingress
## NAMESPACES
```
kubectl get namespace [NS NAME]
kubectl create namespace [NS NAME]
kubectl get -n [NS NAME] pod
curl -v http://[SERVICE NAME].[NS NAME].svc.cluster.local/status/200
```
## CONFIGMAPS & SECRETMAPS
```
Environment name is "SERVICE_VERSION"
Filename and Path is "/config/config.yaml"
```