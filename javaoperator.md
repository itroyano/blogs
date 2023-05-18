Igor Troyanovsky

# Java Operator SDK: Scaffolding Kubernetes operators in Java

## What is a Kubernetes operator?

Operators are software extensions to Kubernetes that make use of custom resources to manage applications and their components. Operators follow Kubernetes principles, notably the control loop.
The operator pattern concept lets you extend the cluster's behaviour without modifying the code of Kubernetes itself by linking controllers to one or more custom resources. Operators are clients of the Kubernetes API that act as controllers for a Custom Resource.

The aim is to code the knowledge of a human operator who is managing a service or set of services. Human operators who look after specific applications and services have deep knowledge of how the system ought to behave, how to deploy it, and how to react if there are problems.

Additional information can be found here:
- https://kubernetes.io/docs/concepts/architecture/controller/
- https://kubernetes.io/docs/concepts/extend-kubernetes/#extension-patterns
- https://kubernetes.io/docs/concepts/extend-kubernetes/operator/

## Why use Java?

While Golang remains the most widely used language for implementing operators and controllers, not everyone is necessarily familiar with its concepts or its pointers and references style similar to C.

Java is very common in the software world, uses a Virtual Machine to seperate the programmer from the hardware, and highly human-readable with its Object-Oriented concepts.
Also, the popular Kubernetes client used in Java - `Fabric8` - has capabilites resembling Golang's clients. We will touch on this in a bit.

## The Java Operator SDK

The [Operator SDK](https://sdk.operatorframework.io/docs/overview/) is capable of automatically generating a lot of the boiler-plate code needed for an operator implementation. This allows the user to focus on modeling and coding the knowledge, without worrying about network interaction with Kubernetes etc'.
Plugins are supported to extend the SDK's options. We will focus specifically on the `quarkus` plugin.

### Wait... Quarkus?

The [Quarkus Java Framework](https://quarkus.io/) stands for fast application start-up times, low memory consumption and lower space requirements for native images. This should get our Operator up and handling our custom resources efficiently.
Quarkus also uses [GraalVM](https://www.graalvm.org/) which supports changing code while the application is running.

## Let's get started

### Prerequisites
- Operator SDK should be installed on your system.
- Maven should be installed.
- Connection to a Kubernetes or OpenShift cluster via Kube Config.
- An IDE you are comfortable with should be available. in this example we will use VSCode with common Java extensions.
- Follow the links in the introduction above to familiarize with the `Group Version Kind` concept of Kubernetes resources.

### Step 1: Scaffolding our first Java Operator

### Step 2: Custom Resources in Java code

### Step 3: The Reconciler and how Fabric8 client helps us implement it

### Step 4: Testing out a custom resouce (with live coding)

## Wrap Up!
