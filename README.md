**this project is do demonstrate how to use ansible to deploy an app to k8 cluster**

some of the challenges faced durnig building the project:
- make docker rootless
- minikube delegation
- tunnel for minikube and bind the address
- insecure registry with minikube

and here is some references:
- https://docs.docker.com/engine/security/rootless/
- https://github.com/kubernetes/minikube/issues/14871#issuecomment-1232505089
- https://minikube.sigs.k8s.io/docs/commands/tunnel/
- https://github.com/kubernetes/minikube/issues/604#issuecomment-247810971