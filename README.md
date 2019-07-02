# Introductions
This is a basic training course for kubernetes. It will use a mix of off the shelf materials and customized ones for cortex developers.

## Lessons
1. [Installing kubernetes](./1-installing/README.md)
      * asdf - install and manage command line utilities: kubectl, helm, minikube
      * Minikube startup and usuage
2. [Kubernetes basics](./2-basics/README.md)
      * Using kubectl
      * Connecting to a cluster
      * Common resources
          - Pods
          - Services
          - Deployments
          - Volumes
          - Secrets
          - Config Maps
          - Cluster Roles
          - Role bindings
      * Port forwarding
3. Developing on Kubernetes
    - Basic infra structure
    - Opening ports
    - Redirect services to IDE
4. Using Helm
    * Helm basics
5. Developing Helm charts
    * GO templates
    * Cortex helm charts
6. Advanced kubernetes
    - Scaling          
    - Stateful sets
    - Daemon sets
    - Rolling upgrades
7. Istio and envoy
    - What and Why ? Service mesh explained
    - Basic Deployment
    - Configuring Istio routing
    - Tracing
    - Metrics
    - Kiali
    - Security
    - Filtering rules
8. Extending Kubernetes
    - Custom resource definitions
    - Controllers
    - APIS
    - Kubebuilder/operators
9. CI/CD with kuberenetes
  - Blue/green deployments
  - Spinnaker
  - Argo
     - ci/cd
     - workflow
     - events


## Reference
- https://kubernetes.io/docs/tutorials/kubernetes-basics/
- 12 factor apps

# Possible decks
Best so far, need to reorder a bit
https://docs.google.com/presentation/d/1zrfVlE5r61ZNQrmXKx5gJmBcXnoa_WerHEnTxu5SMco/edit#slide=id.g309fc81a05_0_205

A bit inverted about pods/services
https://www.slideshare.net/lestrrat/kubernetes-in-30-minutes-20170310
