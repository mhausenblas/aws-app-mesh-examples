# App Mesh with EKS—EC2 inter-services

NOTE: Before you start with this part, make sure you've gone through the [base deployment](base.md) of App Mesh with EKS. In other words, the following assumes that an EKS cluster with App Mesh configured is available and the prerequisites (`aws`, `kubectl`, `jq`, etc. installed) are met.


```bash
$ kubectl -n appmesh-demo apply -f eks-color-example.yaml

# create a color-mesh.svc.cluster.local namespace in Cloud Map

$ source ec2-eks.env
$ ./vpc.sh
$ ./ec2-cluster.sh
```