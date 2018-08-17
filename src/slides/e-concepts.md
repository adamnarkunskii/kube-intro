
class: center, middle

### (short detour)
### 🚨

---

# Containers 🐳

--

## .center[Package Software into Standardized Units for Development, Shipment and Deployment]

🐾

---

# Containers 🐳

A container image is a lightweight, standalone, executable package of software that includes *everything* needed to run an application: 

--

- code,

--

- runtime,

--

- system libraries,

--

-  and settings.

🐾

---

# Containers 🐳

.center[The most widespread and de-facto standard container runtime is

# DOCKER

but that's for another talk.]


🐾

---

class: center, middle

### (back to k8s)
### ⚓

---

# Kubernetes Concepts

--

- Pods 🤖

--

- Controllers 👮‍♀️

--

  - Deployments 🏪

  - Jobs (run to completion) 🎟

  - ...

--

- Services ⛩

--

- Configuration, Networking, Ingress, ... 

🐾

---

# Pods 🤖

--

#### The _Pod_ is the basic building block of Kubernetes.

--

#### The smallest deployable object.

--

#### Represents a running process in your cluster.

--

#### Encapsulates storage and network resources, and options that govern how the container(s) should run.

--

#### A pod can run a single container,

--

#### Or run multiple containers that work together.


🐾

---

# Pods 🤖

.center[
![:scale 40%](https://d33wubrfki0l68.cloudfront.net/aecab1f649bc640ebef1f05581bfcc91a48038c4/728d6/images/docs/pod.svg)

_a multi-container pod with a shared volume_

]

---

# Pods 🤖

--

#### Pods simplify application deployment and management by providing a higher-level abstraction than the set of their constituent applications.

--

#### Pods serve as unit of deployment, horizontal scaling, and replication.

--

#### These handled automatically for containers in a pod:

--

- Colocation (co-scheduling), 

--

- shared fate (e.g. termination), 

--

- coordinated replication, 

--

- resource sharing, 

--

- and dependency management

🐾

---

# Controllers 👮‍♀️

#### A controller is a reconciliation loop that drives actual cluster state toward the desired cluster state.

--

#### For example, a _Replication Controller_, handles replication and scaling by running a specified number of copies of a pod across the cluster.

--

#### A _Job Controller_ creates one or more pods and ensures that a specified number of them successfully terminate.

--

#### Other kinds of controllers include  _Deployment_, _Node Controller_, and _DaemonSet_.

🐾

---

# Services ⛩


#### Kubernetes Pods are mortal. They are born and when they die, they are not resurrected.

--

#### While each Pod gets its own IP address, even those IP addresses cannot be relied upon to be stable over time.

--

#### Then how pods can keep communicating with each other over time?

🐾

---

# Services ⛩

### A Kubernetes Service is an abstraction which defines a logical set of Pods, and the means to access them.

🐾

---

# Services ⛩

.center[
![:scale 60%](https://cdn-images-1.medium.com/max/1000/1*KIVa4hUVZxg-8Ncabo8pdg.png)
]

---
