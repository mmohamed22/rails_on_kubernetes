# Rails on Kubernetes

1- Create a secret to store postgres username and password:
  ```
  $ kubectl create secret generic db-user-pass --from-literal=password=yourpassword
  $ kubectl create secret generic db-user --from-literal=username=drkiq
  ```
  
2- Deploy postgres:
  ```
  $ kubectl create -f postgres.yaml
  ```
  
3- Deploy redis:
  ```
  $ kubectl create -f redis.yaml
  ```
4- Create a secret to store secret-key-base:
  ```
  $ kubectl create secret generic secret-key-base --from-literal=secret-key-base=asecuretokenwouldnormallygohere
  ```
5- Create kube job:
  ```
  $ kubectl create -f job.yaml
  ```
6- Deploy rails:
  ```
  $ kubectl create -f rails.yaml
  ```
7- Deploy sidekiq:
  ```
  $ kubectl create -f sidekiq.yaml 
  ```
  
