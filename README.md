## How to install Kubernetes



### You need to install 3 components
- Virtualbox https://tecadmin.net/install-oracle-virtualbox-on-ubuntu/
- Kubectl https://kubernetes.io/docs/tasks/tools/install-kubectl/
- Minikube https://github.com/kubernetes/minikube/releases https://github.com/kubernetes/minikube

#### Install Virtual Box
```
sudo nano /etc/apt/sources.list
deb http://download.virtualbox.org/virtualbox/debian xenial contrib
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
sudo apt-get update
sudo apt-get install virtualbox-5.1
```

#### Install Kubectl
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

#### Install Minikube
```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.20.0/minikube-linux-amd64
chmod +x minikube
sudo mv minikube /usr/local/bin/
```

#### Minikube Commands
```
minikube start
minikube stop

```

###### Reference
- https://kubernetes.io/docs/getting-started-guides/minikube/
- https://github.com/kubernetes/minikube/releases
