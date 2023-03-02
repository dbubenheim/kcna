# Kubernetes Fundamentals (46%)

The basics of Kubernetes1

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

* [Worker Node]() - responsible for running container workloads
    * [Container Runtime](https://kubernetes.io/docs/concepts/overview/components/#container-runtime) - software that
      runs containers. Kubernetes supports container runtimes such as containerd, CRI-O, and any other implementation of
      the [Kubernetes Container Runtime Interface (CRI)](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-node/container-runtime-interface.md)
    * [kubelet](https://kubernetes.io/docs/concepts/overview/components/#kubelet)
    * [kube-proxy](https://kubernetes.io/docs/concepts/overview/components/#kube-proxy)
* Control Plane - set of components that manage the cluster
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
TBD

## Containers
TBD

## Scheduling
TBD