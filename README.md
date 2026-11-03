# Lab 3 — hello-app on Kubernetes with Terraform

Name: Ravigovinda Bhat Mullankochi
 
Roll number: 261100680017

## Part 1: first `terraform plan`

Paste the `Plan:` line and the summary above it.

```
Terraform Plan:
Plan: 2 to add, 0 to change, 0 to destroy.

Resources:
1. kubernetes_deployment_v1.hello
2. kubernetes_service_v1.hello
```

## Part 1: `terraform output -raw url`

```
http://localhost:8080
```

## Part 2: plan for the v1 → v2 image change

Paste the lines that show the image change, and the `Plan:` line.

```
~ image = "shripada/hello-app:v1" -> "shripada/hello-app:v2"

Plan: 0 to add, 1 to change, 0 to destroy.
```

## Part 3: plan that found the drift after `kubectl scale`

```
~ replicas = "5" -> "3"

Plan: 0 to add, 1 to change, 0 to destroy.
```

## Part 4: `kubectl get svc -A` showing dev and prod

```
NAMESPACE     NAME         TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)
default       kubernetes   ClusterIP   10.96.0.1      <none>        443/TCP
dev           hello-app    NodePort    10.96.40.159   <none>        8080:31336/TCP
kube-system   kube-dns     ClusterIP   10.96.0.10     <none>        53/UDP,53/TCP,9153/TCP
prod          hello-app    NodePort    10.96.36.192   <none>        8090:31183/TCP
```

## Break it: the error after deleting `terraform.tfstate`

```

```

## Break it: the wrong selector

What did you see, and how did you find the cause? One or two sentences.



## Screenshot

Save a browser screenshot as `screenshot.png` in the repository root.
