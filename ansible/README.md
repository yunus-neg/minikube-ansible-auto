**ansible**

this ansible folder conatin roles folder and inventory file and playbooks:

- **roles**
  - **docker**
    - install docker
    - make it rootless (for minikube)
    - add insecure registry in daemon.json
    - deploy, build and push images
  - **minikube**
    - install minikube
    - enable delegation to make minikube work
    - install kubectl
    - start minikube
    - start minikube tunnel for 600 second
    - apply deployment to minikube cluster
    - apply a loadbalancer service to minikube cluster
- **full.yml playbook**
  - this playbook is a oneclick solution to apply it in a freshly installed ubuntu 22, this will do the following:
    - install docker
    - make docker rootless
    - deploy docker registry
    - build and push the app to the registry
    - install minikube
    - enable delegation to make minikube work
    - install kubectl
    - start minikube
    - start minikube tunnel for 600 second
    - apply the deployment for the app
    - apply the loadbalancer service for the app
    - show the url to access the app
- **deploy.yml playbook**
  - build and push the app to the registry
  - start minikube tunnel for 600 second
  - apply the deployment for the app
  - apply the loadbalancer service for the app
  - show the url to access the app
- **inventory**
  - this is the inventory for ansible
- **ansible.cfg**
  - ansible configuration


**how to use it:**

**NOTE:** before running it you need to change the ssh user located in the inventory file

to run it on a freshly installed ubuntu:

`ansible-playbook -i inventory -kK full.yml`

to redeploy the app again:

`ansible-playbook -i inventory -kK deploy.yml`


NOTE: this was tested in ubuntu 22
