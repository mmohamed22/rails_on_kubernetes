# Rails on Kubernetes
Create a secret to store postgres username and password:
$ kubectl create secret generic db-user-pass --from-literal=password=yourpassword
$ kubectl create secret generic db-user --from-literal=username=drkiq
