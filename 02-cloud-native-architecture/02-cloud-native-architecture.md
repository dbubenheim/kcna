# Cloud Native Architecture (16%)

Application architecture in a cloud native world

* Cloud Native Architecture seeks to design systems that support the goal of cloud native technology
* Cloud Native technology is important because it removes roadblocks to innovation, through
    * Software agility
    * Automation
    * Robust, reliable systems
* Examples
    * loosely coupled microservices
    * DevOps
    * Operational automation
    * Serverless
    * Orchestration
* Innovate quickly without breaking things

## Autoscaling

* Autoscaling is the ability to automatically assign more or fewer compute resources to a system to meet demand
* Cost advantages
    * Scaling too low - system/application is not reliable and performance is bad
    * Scaling to high - higher costs
    * Autoscaling - accurate scaling at all times, the best performance and reliability at lowest cost
* metrics are being used to make scaling decisions

### Vertical vs. Horizontal Autoscaling

| vertical scaling                                 | horizontal scaling                         |
|--------------------------------------------------|--------------------------------------------|
| adding resources to existing apps/servers        | adding additional replicas of apps/servers |
| adding more compute power per instance           | adding more instances of an application    |
| adding additional CPU or memory to cluster nodes | adding new nodes to the cluster            |

### Kubernetes Autoscaling Tools

* [Horizontal Pod Autoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/) (HPA) monitors
  resource usage of existing replicas and creates/deletes replicas when needed
* Horizontal Pod Autoscaler (HPA) monitors resource usage of existing replicas and creates/deletes replicas when needed
* Cluster Autoscaler adds and removes nodes from the cluster based on real-time usage

## Serverless

* Serverless is a framework that allows developers to build and run applications without worrying at all about servers
  and server-related concerns like operating systems
* Serverless is sometimes called "Function as a Service (FaaS)"
* Serverless does not mean no servers
    * developers don't have to think about
    * servers are managed by cloud providers
    * resources are provided as needed
    * developers only supply their code
* Examples of serverless
    * AWS Lambda
    * Azure Functions
    * Google Cloud Functions

## Community and Governance

* Cloud Native Communities are groups of individuals who work together to build and promote vendor-neutral cloud native
  technologies, standards and techniques
* One example of Cloud Native communities is the [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/)
    * founded in 2015
    * one of the largest communities (> 153k contributors)
    * manages some of the most widely used projects such as Kubernetes, Prometheus or Envoy
    * defines three stages of project maturity
        * sandbox
        * incubating
        * graduated
* CNCF Governance
    * Governing board
    * The [Technical Oversight Committee (TOC)](https://www.cncf.io/people/technical-oversight-committee/)
        * provides technical leadership to the cloud native community
        * admits new open-source projects to the CNCF
        * aligning projects and removing or archiving projects
    * Decisions are made through **public discussions and voting**
* CNCF Community
    * End User Community provides feedback from users
    * Special Interest Groups (SIG) oversee and coordinate needs for specific domains or technologies
    * Work groups

## Roles and Personas

* roles that interact with cloud native technology in different ways
* not necessarily individuals or positions, but roles fulfilled with respect to the cloud landscape

### Developers

* writes application code
* ensures code works as expected

### Ops

* builds and maintains the infrastructure that runs the code
* deploys the code

### Site Reliability Engineer (SRE)

* Maintains application reliability and performance
* Creates and maintains SLOs, SLAs and SLIs

### Security and Compliance Engineer

* develops and maintains security standards
* ensures application and infrastructure comply with technology and governmental standards

## Open Standards

* a technology specification open to public adoption
* document that describes..
* technologies that support the same open standard can work together more easily
* Open Container Initiative (OCI)
    * Organization that creates open standards for container formats and runtimes
    * Image-spec is an OCI open standard for container image formats
    * Runtime-spec is an OCI open standard for container runtimes
    * The reference implementation for the OCI runtime-spec is **runc**
* Examples of open standards
    * HTML
    * XML
    * OCI runtime-spec and image-spec
    * Kubernetes Service Mesh Interface (SMI)
