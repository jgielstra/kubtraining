# Getting started

## Installing kubernetes virtual machine
Kubernetes requires a linux machine and container runtime ( e.g. docker ) to run.
We will need to install and configure a server to run kubernetes.  
`minikube` simplifies this for us and we will be using `minikube` during this trainining
To use `minikube` will need to install a virtual machines, here are two options:
### Option A) Installing minikube and Virtual Box
    Install VirtualBox
    ```
      brew cask install virtualbox
    ```  
    Install minikube via asdf
    Follow instructions on: https://asdf-vm.com/#/core-manage-asdf-vm?id=install-asdf-vm
    After modifying your bash/zsh profile, reopen terminal to apply changes
    Test `asdf`
    ```
      asdf plugin-list-all
    ```
    Install `minikube` plugin, and configure it
    ```
       asdf plugin-add minikube
       asdf list-all minikube
       asdf install minikube 1.2.0
       asdf global minikube 1.2.0
    ```
### Option B) Installing docker for mac (edge channel)

## Installing additional command line tools
To work against a kuberenetes cluster we need to install a few command-line utilities.
The most important one is kubectl.
### option A) installing using asdf
`asdf` version manager
This is an optional setup but it is very convenient for managing versions of utilities.
```
  asdf plugin-add kubectl
  asdf install kubectl 1.15.0
  asdf global kubectl 1.15.0

  asdf plugin-add minikube
  asdf install minikube 1.2.0
  asdf global minikube 1.2.0

  asdf plugin-add helm
  asdf install helm 2.14.1
  asdf global helm 2.14.1

```

### option B) installing using brew
```
brew install minikube
brew install kubectl
brew install helm
```

Optional installs
```
brew install kubectx
brew install stern
brew install k9s
```

Verify correct version of utilities
```
$ kubectl version --client   
Client Version: version.Info{Major:"1", Minor:"15", GitVersion:"v1.15.0", GitCommit:"e8462b5b5dc2584fdcd18e6bcfe9f1e4d970a529", GitTreeState:"clean", BuildDate:"2019-06-19T16:40:16Z", GoVersion:"go1.12.5", Compiler:"gc", Platform:"linux/amd64"}

$ minikube version
minikube version: v1.2.0

$ helm version --client
Client: &version.Version{SemVer:"v2.14.1", GitCommit:"5270352a09c7e8b6e8c9593002a73535276507c0", GitTreeState:"clean"}
```

Testing the minikube kubernetes cluster
```
$ minikube status
host: Running
kubelet: Running
apiserver: Running
kubectl: Correctly Configured: pointing to minikube-vm at 192.168.99.108

$ kubectl get -A nodes
NAME       STATUS   ROLES    AGE   VERSION
minikube   Ready    master   24m   v1.15.0
```
