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
    * is a project within the linux foundation founded in 2015
    * one of the largest communities (> 153k contributors)
    * manages some of the most widely used projects such as Kubernetes, Prometheus or Envoy
    * defines three stages of project maturity
        * sandbox
          * project in a very early stage which has significant community involvement
          * adopted because it offers unrealized potential
          * receives minimal funding
          * will be removed within 12 months if
        * incubating
          * project will become incubated if it shows growth and maturity
          * at least three companies use it in production
          * accept regular contributions from the community
        * graduated
          * can be voted by the Technical Oversight Commitee (TOC)
          * have shown their adoption in the past
          * have committers from at least two big companies
          * meet the Linux Foundation best practices
* CNCF minimal viable governance
    * Governing board
    * The [Technical Oversight Committee (TOC)](https://www.cncf.io/people/technical-oversight-committee/)
        * provides technical leadership to the cloud native community
        * approves new open-source projects
        * aligning projects and removing or archiving projects
        * defines common practices
        * maintains the technical vision
    * Decisions are made through **public discussions and voting**
* CNCF Community
    * End User Community provides feedback from users
    * Special Interest Groups (SIG) oversee and coordinate needs for specific domains or technologies
    * Work groups

## Job Roles and Personas

* roles that interact with cloud native technology in different ways
* not necessarily individuals or positions, but roles fulfilled with respect to the cloud landscape

### Cloud Architect

* designs the cloud architecture

### DevOps Engineer

* builds and maintains the infrastructure that runs the code
* deploys the code

### Full Stack Developer

* writes application code
* ensures code works as expected
* takes care of the entire stack

### Site Reliability Engineer (SRE)

* Maintains application reliability and performance
* Creates and maintains SLOs, SLAs and SLIs

### Security and Compliance Engineer

* develops and maintains security standards
* ensures application and infrastructure comply with technology and governmental standards

### Data Engineer

* manages large amounts of data in cloud environments

### DevSecOps Engineer

* responsible for the application lifecycle including security

## Open Standards

* a technology specification open to public adoption
* open standards guarantee interoperability and are common in cloud native
* based on open source technology to prevent vendor lock-in
* document that describes..
* technologies that support the same open standard can work together more easily
* Open Container Initiative (OCI)
    * Linux Foundation project started by Docker in 2015
    * creates open standards for container formats and runtimes
* examples of open standards
    * Containers are the standard for packaging applications
    * Image-spec is an OCI open standard which defines how to build and package container images
    * Runtime-spec is an OCI open standard to define how to run a container
    * Kubernetes Service Mesh Interface (SMI)
    * Container Network interface (CNI) specifies how to implement network for containers
    * Container Runtime Interface (CRI) defines how to implement container runtimes in orchestration systems
    * Container Storage Interface (CSI) specifies how to implement storage in containers
    * Service Mesh Interface (SMI) defines how to implement service mesh in orchestration systems
    * Hypertext Markup Language (HTML)
    * Extensible Markup Language (XML)

## Links

* https://aws.amazon.com/what-is/cloud-native/