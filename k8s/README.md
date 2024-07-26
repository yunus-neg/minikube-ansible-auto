**Kubernetes**

this folder has two files:

- **deployment**
  - deplyment file to deploy the app to k8s cluster
- **service**
  - service file to access the app using loadbalancer

to use the apply the file to your cluster:
`kubectl apply -f <file_name>`

**NOTE:** this not the actual files that is useb by the ansible these files are just a reference, because in ansible it more dynamic
