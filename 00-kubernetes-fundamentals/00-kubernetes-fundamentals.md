# Kubernetes Fundamentals (46%)

The basics of Kubernetes

## Kubernetes Resources

* A resource is an object of certain type in the Kubernetes API
* `kubectl api-resources` lists all available resource types in the cluster
* `Pods` are the smallest deployable units of computing that you can create and manage in Kubernetes
* A `Deployment` provides declarative updates for `Pods` and `ReplicaSets`
* A `Service`is an abstract way to expose an application running on a set of Pods as a network service
* Available types of `Services` are
    * `LoadBalancer`
    * `NodePort`
    * `ClusterIp`
    * `ExternalName`
* A `ReplicaSet`'s purpose is to maintain a stable set of replica `Pods` running at any given time
* You can create a custom resource with the `CustomResourceType`
* `kubectl explain` gives documentation about specified resources
* To run a task before the main container starts up we can use
  an [Init Container](https://kubernetes.io/docs/concepts/workloads/pods/init-containers/)

## Kubernetes Architecture

![cluster-architecture](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg)

* [Worker Node](https://kubernetes.io/docs/concepts/overview/components/#node-components) - responsible for running
  container workloads
    * [Container Runtime](https://kubernetes.io/docs/concepts/overview/components/#container-runtime) - software that
      runs containers. Kubernetes supports container runtimes such as containerd, CRI-O, and any other implementation of
      the [Kubernetes Container Runtime Interface (CRI)](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-node/container-runtime-interface.md)
    * [kubelet](https://kubernetes.io/docs/concepts/overview/components/#kubelet)
    * [kube-proxy](https://kubernetes.io/docs/concepts/overview/components/#kube-proxy)
* [Control Plane](https://kubernetes.io/docs/concepts/overview/components/#control-plane-components) - set of components
  that manage the cluster
    * [etcd](https://kubernetes.io/docs/concepts/overview/components/#etcd) - distributed (etc directory) object storage
      used by the API Server
    * [kube-apiserver](https://kubernetes.io/docs/concepts/overview/components/#kube-apiserver) - center of the control
      plane used for cluster communication
    * [kube-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#kube-controller-manager) - runs
      controller processes
    * [kube-cloud-controller-manager](https://kubernetes.io/docs/concepts/overview/components/#cloud-controller-manager)
        - embeds cloud-specific control logic
    * [kube-scheduler](https://kubernetes.io/docs/concepts/overview/components/#kube-scheduler) - watches for newly
      created `Pods` with no assigned node, and selects a node for them to run on

## Kubernetes API

* The core of Kubernetes' control plane is the API server
* The Kubernetes API lets you query and manipulate the state of API objects in Kubernetes
* The Kubernetes API is a resource-based (RESTful) programmatic interface provided via HTTP
* New features enter the API as alpha features, progress through beta, and eventually graduate to stable
* Kubernetes has a deprecation policy that guarantees all stable objects will be supported for at least 12 months, or
  two releases (whichever is longer), after deprecation
*

## Containers

* containers decouple applications from underlying host infrastructure
* a container image is a ready-to-run software package, containing everything needed to run an application
* containers are intended to be stateless and immutable
* each node in a Kubernetes cluster runs the containers that form the Pods assigned to that node
* a pod is a thin wrapper around one or more containers
* containers must be wrapped into Pods if they want to run on k8s
* containers in a pod share the same environment and are guaranteed to be scheduled on the same node

## Scheduling

* In Kubernetes, scheduling refers to making sure that Pods are matched to Nodes so that Kubelet can run them
* A scheduler watches for newly created Pods that have no Node assigned
* [kube-scheduler](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/#kube-scheduler) is the
  default scheduler for Kubernetes and runs as part of the control plane
* Kube-scheduler selects an optimal node to run newly created or not yet scheduled (unscheduled) pods

